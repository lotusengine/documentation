---
path: "/docs/general/concepts"
title: Core Concepts
---

## Workflows


### What are workflows?

Workflows are the core concept of LotusEngine. These automations aim to let you connect to 3rd party services, manipulate data, etc. You can use them to create smart pricing systems based on demand, to connect one service to others based on complex logic, and so on.  

Workflows can be thought of as flowcharts that let you connect blocks of functionality with logic. These blocks can connect to 3rd party services, store and manipulate data and so on.


### How are workflows launched?

LotusEngine lets you trigger automations based on many signals or methods. These can be scheduled, triggered using the API, called from JavaScript code on another site as well as in reaction to data insights such as order volume, new lead added, repeat visitor, etc. 




## Channels


### What are channels?

In order to let you launch automations based on as many signals as possible such as order volume, best selling item, etc we have the concept of _channels_ which are just the types of data found in ecommerce and marketing.

We currently support:

- *Orders*: transactions and their related items/customers
- *Leads*: sale opportunities
- *Visits*: website visitor and related visit data
- *Events*: generic event such as button clicks, video views, etc
- *Forms*: form submissions
- *Subscriptions*: mailing list subscriptions

By understanding these models we can provide greater insight on which you can trigger your automations with.

In addition, by delineating a standard format or CDA (Canonical Data Model) for things like order data we can build reusable functionality or integrations that can be shared with the community.

Let's imagine that a developer creates workflows to receive orders from Shopify, eBay and Amazon. By using a standard model for these orders, the developer can write workflows without being concerned about how each of these sources formats their orders. Along the same lines, integrations are developed to work with these channels - for example, a SendGrid email receipt integration knows where to find the email property in a provided order object.

