---
id: intro
title: Workflow Overview
---


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
