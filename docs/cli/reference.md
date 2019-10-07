---
path: "/docs/cli/reference"
title: CLI Reference
---
 

##  Overview

LotusEngine offers a few different types of storage for you to develop with. Let's take a look - we have storage for:
- Channel data
- Tabular data
- Encrypted key

Let's go over each one.

## Channel Storage


Storing channel data refers to the storage of the incoming stream such as orders, contacts etc... This data can be queried using the GraphQL API. Please refer to those docs.

##  Encrypted Key Storage

The LotusEngine Encrypted Keys - or LEEK :) - is a simple key value store to manage data such as api keys and such. One of its main intended use is to to allow 3rd party clients or other LE users to share sensitive data that can be used safely in workflows. This means the workflow developer cannot see the keys nor is there a concern of the data accidentally being leaked out as it can only be used within the context of a particular developers workflows.

## Converting data into a leek

This can be done through the UI or the CLI toolbelt. 

```shell
lotus leek create --data "My Secret"
// Will echo an ID - ex: 73106750-c8ed-11e9-9c54-cfa66bf24f72
```

This ID can then be used in workflows as `LK:73106750-c8ed-11e9-9c54-cfa66bf24f7` and will automatically be replaced by "My Secret". 

### Managing 3rd party data

Now while this addresses the issue of having sensitive data in the workflows from being exposed accidentally (i.e. a GitHub push) it doesn't handle hiding the data from the developer if obtained from a 3rd party client. 

To handle this a developer can generate a request for a link that can be sent to a client. Upon following this link the client will be presented with a secure form to enter their sensitive data. Submitting this form will send an email to the developer with the leek IDs necessary to use in the workflow.

```shell
lotus leek request -k "Your something API key" -k "Your other secret I need" -e client@example.org
// Will echo a URL to send to client
```


## Parameter Storage

While channel data is meant to handle the stream of orders, analytics etc there is often the need to refer to some kind of CSV/tabular data when developing workflows. For example, if you wanted to reference [Google Shopping categories](https://support.google.com/merchants/answer/6324436?hl=en) in your code you could upload the CSV/Excel data and have it available as a simple flat table to query.


## Table operations
### Creating tables

To create a new table, pass the desired name as well as the name of header columns. You can also create the header columns on the fly upon your initial CSV upload. Note that subsequent uploads my error out if the column count is not consistent with initial headers created.

```shell
lotusengine table create --title 'My Cats' --headers 'ID|Name of Cat|Something Else|`
```

### Deleting tables
This operation will wipe the data and the table itself.

```shell
lotusengine table delete --title 'My Cats' 
```
### Clearing tables
This operation will wipe the data but keep the table and header info.

```shell
lotusengine table clear --title 'My Cats' 
```

### Appending CSV data
This operation will append new data to the table.

```shell
lotusengine table append --title 'My Cats' --data 'the data - you can also pipe from stdin'
```

## Data constraints

### Field type and length
Each field must be a string or float and cannot exceed 500 characters

### Uniqueness

While there is nothing preventing you from repeating the same data in some fields keep in mind that querying always returns a single row (the first match). Query and format your data accordingly.

## Querying the table

### From (worker)[workers] code
```javascript
import { getParameter } from './core';
export default async function(event) {
  const row = await getParameter('foo')
}
```
Refer to (worker)[workers] docs for exact syntax.



##  Workflows

Workflows are the heart of LotusEngine. They define how your app will work - from webhook to storage to integrations. A workflow can be defined as a configuration file using JSON/YAML or through the LotusEngine UI. They can be exported, imported and shared.

Take a look at a basic workflow:

```
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


##  Workflow Triggers

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
      "keys": [
        "e3d5e160-ac8a-11e9-8742-0d36cbe54355"
      ]
    },
    {
      "origins": [
        "*"
      ]
    }
  ]
}
```


#### Parameter definition

 Parameter    | Default | Description                                                                      |
| ------------ | ------- | -------------------------------------------------------------------------------- |
| active | false   | Enable/disable webhook.                               |
| keys    |  null   | Array of UUID. Valid UUID Version 1 to use as keys for header validation. The header to send is `x-lotus-wid`. You can generate these keys yourself using `uuidgen` on the MacOS/Linux CLI or use an online generator such as https://www.uuidgenerator.net. |
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


Parameter | Type | Default | Required | Description
---------- | -------
active | boolean | false | N | Whether to enable webhook functionality
origins | array | [] | N | List of origin domains. ex: `example.org` or '.example.org' to match subdomains.
keys | array | false | N | List of UUIDv1 keys to pass in header or query param.

*Note*: origins and keys restrictions are cumulative.

## Creating keys
Keys are simply tokens in the UUIDv1 format (ex: 9e9c72b0-d8c9-11e9-aca6-d7f551bd8a12). You can generate them yourself (online)[https://www.uuidgenerator.net/version1] or on MacOS/*nix using the `uuidgen` command.

```bash
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

Workers are *not* NodeJS code but instead pure JS with some added functionality such as logging, fetch etc... 

Your worker code accepts one parameter, _event_, which is an object containing the current payload and whatever workflow parameters you have defined.

< Example worker to send an email through SendGrid.
```javascript
export default async function(event) {
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

### `logMessage'

Send a message to debug logs.

    import { logMessage } from 'core'


#### Parameters

Parameters | Required | Type | Description
---------- | -------- | ---- | -----------
message | yes | string | Message to send to console

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
export default async function(event) { 
  const row = await getParameter('users', 'email', 'foo@example.org')
}
```
#### Parameters

Parameters | Required | Type | Description
---------- | -------- | ---- | -----------
table | yes | string | Sheet or table name
field | yes | string | Column name
value | yes | string | Column value

#### Sample response
```json
{ 
  "id": 123,
  "name": "Jon",
  "email": "foo@example.org",
  "hobby": "coding",
}
```
  


## Exporting

 
*Note* This is a wip feature.

We are currently working on the option to export workflows as Docker containers to run as standalone services on your own servers. Stay tuned.