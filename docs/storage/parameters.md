---
path: "/docs/storage/parameters"
title: Parameter Storage
---

While channel data is meant to handle the stream of orders, analytics etc there is often the need to refer to some kind of CSV/tabular data when developing workflows. For example, if you wanted to reference [Google Shopping categories](https://support.google.com/merchants/answer/6324436?hl=en) in your code you could upload the CSV/Excel data and have it available as a simple flat table to query.


## Table operations
### Creating tables

To create a new table, pass the desired name as well as the name of header columns. You can also create the header columns on the fly upon your initial CSV upload. Note that subsequent uploads my error out if the column count is not consistent with initial headers created.

```shell
% lotusengine table create --title 'My Cats' --headers 'ID|Name of Cat|Something Else|`
```

### Deleting tables
This operation will wipe the data and the table itself.

```shell
% lotusengine table delete --title 'My Cats' 
```
### Clearing tables
This operation will wipe the data but keep the table and header info.

```shell
% lotusengine table clear --title 'My Cats' 
```

### Appending CSV data
This operation will append new data to the table.

```shell
% lotusengine table append --title 'My Cats' --data 'the data - you can also pipe from stdin'
```

## Data constraints

### Field type and length
Each field must be a string or float and cannot exceed 500 characters

### Uniqueness

While there is nothing preventing you from repeating the same data in some fields keep in mind that querying always returns a single row (the first match). Query and format your data accordingly.

## Querying the table

### From (worker)[workers] code
```javascript
import { getParameter } from './core';
export default async function(event) {
  const row = await getParameter('foo')
}
```
Refer to (worker)[workers] docs for exact syntax.



