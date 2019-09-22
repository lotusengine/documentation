---
id: webhooks
title: Webhooks
---

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

  