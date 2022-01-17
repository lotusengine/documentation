# Workflows

## Overview

Workflows are the heart of LotusEngine. They define how your app will work - from webhook to storage to integrations. A workflow can be defined as a configuration file using JSON/YAML or through the LotusEngine UI. They can be exported, imported and shared.

Take a look at a basic workflow:

```json
{
  "title": "My workflow",
  "description": "It does so much!",
  "triggers": {
    "webhook": {
      "active": true,
      "keys": ["e3d5e160-ac8a-11e9-8742-0d36cbe54355"],
      "origins": ["example.org"]
    },
    "events": []
  },
  "input": {
    "channel": "leads/1",
    "validation": {},
    "start": "MyFirstStep"
  },
  "steps": {
    "MyFirstStep": {
      "type": "storage"
    }
  }
}
```

## Workflow Modules

Workflows are assembled from a variety of modules. The current module types are:

- Logic - workflow branching based on decisions
- Workers - Javascript code for data manipulation or http calls
- Integrations - 3rd party connectors
- Query - GraphQL queries to fetch & put data
- Events - Trigger events that other workflows can react to
- Notifications - SMS/Email alerts
- Logger - System log

## Workflow Triggers

Here are the ways to launch a workflow:

- webhook
- API call
- from another workflow
- from an event
- using the CLI

### Webhooks

To define a webhook in your workflow add the following section at the base level:

```yaml
webhook:
  - active: true
  - keys:
	  - "e3d5e160-ac8a-11e9-8742-0d36cbe54355"
  - origins:
    - "*"
```

```json
{
  "webhook": [
    {
      "active": true
    },
    {
      "keys": ["e3d5e160-ac8a-11e9-8742-0d36cbe54355"]
    },
    {
      "origins": ["*"]
    }
  ]
}
```

### Parameter Definition

|Parameter | Default | Description | | ------------ | ------- | -- |
| active | false | Enable/disable webhook. |
| keys | null | Array of UUID. Valid UUID Version 1 to use as keys for header validation. The header to send is `x-lotus-wid`. You can generate these keys yourself using `uuidgen` on the MacOS/Linux CLI or use an online generator such as https://www.uuidgenerator.net. |
| origins | null | Array of URLS to allow. Use `*` for wildcard. |

## Webhooks

Workflows can be triggered by 3rd party webhooks. To setup your workflow to accept data from a remote source setup the webhook field under `triggers`:

```json
{
   triggers: {
     webhook: {
       active: true,
       origins: [],
       keys: []
     }
   }
```

| Parameter | Type    | Default | Required | Description                                                                      |
| --------- | ------- | ------- | -------- | -------------------------------------------------------------------------------- |
| active    | boolean | false   | N        | Whether to enable webhook functionality                                          |
| origins   | array   | []      | N        | List of origin domains. ex: `example.org` or '.example.org' to match subdomains. |
| keys      | array   | false   | N        | List of UUIDv1 keys to pass in header or query param.                            |

_Note_: origins and keys restrictions are cumulative.

## Creating keys

Keys are simply tokens in the UUIDv1 format (ex: 9e9c72b0-d8c9-11e9-aca6-d7f551bd8a12). You can generate them yourself [online](https://www.uuidgenerator.net/version1)or on MacOS/\*nix using the `uuidgen` command.

```shell
$ uuidgen
```

## Passing tokens in the request

You can either provide the token in the header (preferred) using the 'Authorization' header and the 'Token' scheme:

    "Authorization: Token 2d4375e0-d8ca-11e9-aca6-d7f551bd8a12"

Alternatively, you can provide the token in the URL using the `token` parameter:

    https://......?token=4f04d160-d8ca-11e9-aca6-d7f551bd8a12

## Workers

Workers allow you to run sandboxed JavaScript code. They can be used to modify your data if you find that the template module is too limited. You can also use it to make remote API calls.

A worker is a simple exported function. You can use ES7/ES8 as we run our code through Webpack.

Workers are _not_ NodeJS code but instead pure JS with some added functionality such as logging, fetch etc...

Your worker code accepts one parameter, _event_, which is an object containing the current payload and whatever workflow parameters you have defined.

< Example worker to send an email through SendGrid.

```javascript
export default async function (event) {
  const { parameters, data } = event

  const { email } = data

  const body = {
    personalizations: [
      {
        to: [
          {
            email
          }
        ],
        subject: 'Hello, World!'
      }
    ],
    from: {
      email
    },
    content: [
      {
        type: 'text/plain',
        value: 'Hello, World!'
      }
    ]
  }

  return fetch('https://api.sendgrid.com/v3/mail/send', {
    method: 'POST',
    body: JSON.stringify(body),
    headers: {
      Authorization: 'Bearer ' + parameters.SENDGRID_API_KEY,
      'Content-Type': 'application/json'
    }
  }).then(res => res.json())
}
```

## Built-in methods

A few methods are packaged as an importable module.

### logMessage

Send a message to debug logs.

    import { logMessage } from 'core'

#### Parameters

| Parameters | Required | Type   | Description                |
| ---------- | -------- | ------ | -------------------------- |
| message    | yes      | string | Message to send to console |

### callApi

To call the LotusEngine GraphQL API.

    import { callApi } from 'core'

### doRequest

To perform XMLHttpRequest requests

    import { doRequest } from 'core'

Note that this is a thin wrapper around the (`axios`)[https://github.com/axios/axios] module. Check out the docs for usage.

### getParameter

Retrieves stored parameter data row by exact match (case insensitive)

```javascript
import { getParameter } from 'core'
export default async function (event) {
  const row = await getParameter('users', 'email', 'foo@example.org')
}
```

#### Parameters

| Parameters | Required | Type   | Description         |
| ---------- | -------- | ------ | ------------------- |
| table      | yes      | string | Sheet or table name |
| field      | yes      | string | Column name         |
| value      | yes      | string | Column value        |

#### Sample response

```json
{
  "id": 123,
  "name": "Jon",
  "email": "foo@example.org",
  "hobby": "coding"
}
```

## Exporting

_Note_ This is a wip feature.

We are currently working on the option to export workflows as Docker containers to run as standalone services on your own servers. Stay tuned.


## Developer tools

- GraphQL API
- CLI
- TypeScript SDK


