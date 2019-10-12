---
path: "/docs/dev/reference"
title: JSONPath Reference
---
 
## What is JSONPath

(JSONPath)[https://goessner.net/articles/JsonPath/] is used to traverse JSON data structures. We use it in a few of our workflow modules such as:
- mapping
- logic

With it we can transform data from a 3rd party source into one of our models and we can also implement basic logic based on our data. 

## JSONPath Syntax


JSONPath          | Description
------------------|------------
`$`               | The root object/element
`@`               | The current object/element
`.`               | Child member operator
`..`	            | Recursive descendant operator; JSONPath borrows this syntax from E4X
 `*`  	          | Wildcard matching all objects/elements regardless their names
`[]`	            | Subscript operator
`[,]`	            | Union operator for alternate names or array indices as a set
`[start:end:step]`| Array slice operator borrowed from ES4 / Python
`?()`             | Applies a filter (script) expression via static evaluation
`()`	            | Script expression via static evaluation 


Example JSONPath expressions:

JSONPath                                         | Description
-------------------------------------------------|------------
`$.store.book[*].author`                         | The authors of all books in the store
`$..author`                                      | All authors
`$.store.*`                                      | All things in store, which are some books and a red bicycle
`$.store..price`                                 | The price of everything in the store
`$..book[2]`                                     | The third book
`$..book[(@.length-1)]`                          | The last book via script subscript
`$..book[-1:]`                                   | The last book via slice
`$..book[0,1]`                                   | The first two books via subscript union
`$..book[:2]`                                    | The first two books via subscript array slice
`$..book[?(@.isbn)]`                             | Filter all books with isbn number
`$..book[?(@.price<10)]`                         | Filter all books cheaper than 10
`$..book[?(@.price==8.95)]`                      | Filter all books that cost 8.95
`$..book[?(@.price<30 && @.category=="fiction")]`| Filter all fiction books cheaper than 30
`$..*`                                           | All members of JSON structure


## Examples

Let's imagine that we have some data coming in our webhook that looks like this:

```json
{
  "order_id": "123",
  "purchase_items": [
    {
      "title": "My Item",
      "code": "SKU111",
      "description": "It is really cool",
      "price": 23,
      "qty": 2
    },
    {
      "title": "My OtherItem",
      "code": "SKU222",
      "description": "It is even cooler",
      "price": 12,
      "qty": 1
    }
  ]
}
```
And let's say that we wanted to transform this data into this:
```json
{
  "transaction": "123",
  "items": [
    {
      "sku": "SKU111",
      "price": 23,
      "quantity": 2
    },
    {
      "sku": "SKU222",
      "price": 12,
      "quantity": 1
    }
  ]
}
```
We could apply this mapping template:
```json
{
  "transaction": "$.order_id",
  "items": [
    "$.purchase_items",
    {
      "sku": "$.code",
      "price": "$.price",
      "quantity": "$.qty"
    }
  ]
}
```

We'll cover more relevant examples in the docs for the respective modules.

