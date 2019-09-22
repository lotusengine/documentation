---
id: workers
title: Workers
---

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
  

