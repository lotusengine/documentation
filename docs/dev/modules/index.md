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
    "errors": {
      "type": "array",
      "items": {
        "type": "object",
        "additionalProperties": false,
        "required": ["code"],
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

The `code` parameter should be written in THIS*FORMAT. Do not add "ERROR" as the system will automatically prepend "ERROR_MODULENAME*" to all returned codes (i.e. if a module name is foo and you return BAD_REQUEST then the full error code is `ERROR_FOO_BAD_REQUEST`.

At the simplest format a simple return statement is equivalent to:

```json
{
  "result": null,
  "errors": [],
  "status": "success"
}
```

A sample response with payload and an error:

```json
{
  "result": { "foo": "bar" },
  "error": [
    {
      "code": "BAD_REQUEST",
      "message": "That did not go well",
      "data": {
        "somedata": "somevalue"
      }
    }
  ],
  "status": "error"
}
```

Example:

```js
let errors = []

try {
  await someConnection()
} catch (e) {
  errors.push({
    code: 'BAD_REQUEST',
    message: 'A bad thing happened',
    data: {}
  })

  // We could return here or continue...
  return {
    errors
  }
}
```

### Response status

The `status` field is used to determine the next course of action. An `error` status will cause the workflow to halt while a `success` status will allow the workflow to continue regardless of any errors returned.

If no status is explicitly provided the default will be `success` unless one or more error exists im which case 'error' will be the default status causing the workflow to halt.

### Error code naming convention

When an error code is returned the system will automatically append `ERROR_MODULENAME_` to the code. This allows you to create trigers for all errors (match: `ERROR`) or all errors from that moodule (`ERROR_MODULENAME`). Therefore do not use `ERROR` in naming the code parameter since it will be done for you.

### Error message and data

While it may be tempting to simply pass a thrown error to the response as in:

```js
try {
  g
  await someConnection()
} catch (e) {
  errors.push({ code: 'BAD_REQUEST', message: e.message, data: e }) // Bad

  errors.push({
    code: 'BAD_REQUEST',
    message: 'A bad thing happened',
    data: { foo: 'bar' }
  }) // Good
}
```

This is not advised. We recommend that you explicitly provide a clear message and only provide the relevant data necessary for workflows to act upon. Stack traces are not useful...
