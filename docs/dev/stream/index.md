---
path: "/docs/dev/stream"
title: The Stream Object
---
 
Throughout a workflow's lifecycle a number of parameters are available for inspection and potential modification. Depending on the type of workflow action involved the manner in which this data is accessed will differ but the structure remains the same.

A workflow action receives stream data that looks like this:
```json
{
  "config": {
    "clientId": "9ca9b4a0-ed68-11e9-8682-61c8188df182",
    ...
  },
  "context": {
    "someCoolVar": "coolness 2.0"
    ...
  },
  "data": {
    "transaction": "123",
    ...
  }
}
```
The stream container contains these nested objects:

### The `config` object
This structure is read-only and contains useful variables such as the clientID.

### The `context` object
The context structure is your storage for the duration of the workflow's lifecycle. It's a place to stash useful data that other workflow actions may use. It is writeable when returning a response such as in the mapping actions.

### The `data` object
This is the channel data you are working with. It usually comes in from a webhook and is the core data you are working with in your workflow. It can be a set channel format such as order, visits etc or some custom structure you are using.