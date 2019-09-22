---
id: triggers
title: Workflow Triggers
---

Here are the ways to launch a workflow:

- webhook
- API call
- from another workflow
- from an event
- using the CLI

### Webhooks

To define a webhook in your workflow add the following section at the base level:

<!--DOCUSAURUS_CODE_TABS-->
<!--YAML-->
```yaml
webhook:
  - active: true
  - keys:
	  - "e3d5e160-ac8a-11e9-8742-0d36cbe54355"
  - origins:
    - "*"
    
```
<!--JSON-->
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
<!--END_DOCUSAURUS_CODE_TABS-->

#### Parameter definition

 Parameter    | Default | Description                                                                      |
| ------------ | ------- | -------------------------------------------------------------------------------- |
| active | false   | Enable/disable webhook.                               |
| keys    |  null   | Array of UUID. Valid UUID Version 1 to use as keys for header validation. The header to send is `x-lotus-wid`. You can generate these keys yourself using `uuidgen` on the MacOS/Linux CLI or use an online generator such as https://www.uuidgenerator.net. |
| origins | null | Array of URLS to allow. Use `*` for wildcard. |
