---
path: "/docs/storage/leek"
title: Encrypted Key Storage
---

The LotusEngine Encrypted Keys - or LEEK :) - is a simple key value store to manage data such as api keys and such. One of its main intended use is to to allow 3rd party clients or other LE users to share sensitive data that can be used safely in workflows. This means the workflow developer cannot see the keys nor is there a concern of the data accidentally being leaked out as it can only be used within the context of a particular developers workflows.

## Converting data into a leek

This can be done through the UI or the CLI toolbelt. 

```shell
% lotus leek create --data "My Secret"
// Will echo an ID - ex: 73106750-c8ed-11e9-9c54-cfa66bf24f72
```

This ID can then be used in workflows as `LK:73106750-c8ed-11e9-9c54-cfa66bf24f7` and will automatically be replaced by "My Secret". 

### Managing 3rd party data

Now while this addresses the issue of having sensitive data in the workflows from being exposed accidentally (i.e. a GitHub push) it doesn't handle hiding the data from the developer if obtained from a 3rd party client. 

To handle this a developer can generate a request for a link that can be sent to a client. Upon following this link the client will be presented with a secure form to enter their sensitive data. Submitting this form will send an email to the developer with the leek IDs necessary to use in the workflow.

```shell
% lotus leek request -k "Your something API key" -k "Your other secret I need" -e client@example.org
// Will echo a URL to send to client
```




