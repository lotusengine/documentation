---
path: '/docs/dev/reference'
title: Storage options
---

## Overview

LotusEngine offers a few different types of storage for you to develop with. Let's take a look - we have storage for:

- Channel data
- Tabular data
- Encrypted key

Let's go over each one.

## Channel Storage

Storing channel data refers to the storage of the incoming stream such as orders, vists, etc... This data can be queried using the GraphQL API. Please refer to [GraphQL API docs](/docs/api/intro).

## Encrypted Key Storage

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

## Sheet Storage

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

```javascript
import { getSheet } from './core'
export default async function (event) {
  const row = await getSheet('foo')
}
```
