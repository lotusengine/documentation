---
path: '/docs/dev/modules'
title: Module reference
---

## Response format

Modules should return an object in the following format:

```json
{
  "type": "object",
  "additionalProperties": false,
  "properties": {
    "events": {
      "type": "array",
      "items": {
        "type": "object",
        "additionalProperties": false,
        "properties": {
          "code": {
            "type": "string",
            "pattern": "^[A-Z][A-Z_0-9]{1,98}[A-Z0-9]$"
          },
          "data": {
            "type": "object",
            "additionalProperties": true,
            "default": {}
          },
          "message": {
            "type": "string",
            "maxLength": 250
          }
        }
      }
    },
    "result": {
      "oneOf": [
        {
          "type": "object"
        },
        {
          "type": "number"
        },
        {
          "type": "string"
        },
        {
          "type": "array"
        },
        {
          "type": "null"
        },
        {
          "type": "boolean"
        }
      ]
    }
  }
}
```

The `code` parameter should be written in THIS_FORMAT and end with "ERROR" for errors.

At the simplest format a simple return statement is equivalent to:

```
{
  result: null,
  events: []
}
```

A sample response with payload, am event to be logged and an error:

```
{
  result: { foo: 'bar' },
  events: [{
    code: 'REQUEST_ERROR',
    message: 'That did not go well',
    data: {
      somedata: 'somevalue',
    }
  }, {
    code: 'LOW_BALANCE',
    message: 'Not an error but something we may want to act on',
  }]
}

```

```

```
