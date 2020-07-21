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
    "status": {
      "type": "string",
      "enum": ["success", "error"]
    },
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

```json
{
  "result": null,
  "events": [],
  "status": "success"
}
```

A sample response with payload, am event to be logged and an error:

```json
{
  "result": { "foo": "bar" },
  "events": [
    {
      "code": "REQUEST_ERROR",
      "message": "That did not go well",
      "data": {
        "somedata": "somevalue"
      }
    },
    {
      "code": "LOW_BALANCE",
      "message": "Not an error but something we may want to act on"
    }
  ],
  "status": "error"
}
```

### Errors vs non errors

The `events` response parameter is for all log entries that may be of relevance. The general recommendation is that if the event occurs as a result of an error being thrown then append `_ERROR`. Non error events can be used for debugging for ex:

```js
let events = []
// Some info we want to log - perhaps based on a debug module option
if(options.debug)
  events.push({
    code: 'SOMETHING',
    message: 'Please make note of this',
    data: { foo: 'bar' }
  })

try {
  await someConnection()
} catch(e) {
  events.push({ code: 'BAD_ERROR', message: 'A bad thing happened', data: { error: e.toString  }))

  // We could return here
  return {
    events
  }
}
```

### Response status

The `status` field is used to determine the next course of action. An `error` status will cause the workflow to halt while a `success` status will allow the workflow to continue regardless of events (and potentially errors) returned.

If no status is explicitly provided the default will be `success` unless one or more error codes (ending in `_ERROR`) exists in the events array.
