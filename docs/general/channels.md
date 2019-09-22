---
path: "/docs/general/channels"
title: Channels
---
### Channel overview

Channels are essentially database models that allow integrations to work with standardized schemas. Having a unified format abstracts the process of working with 3rd party services.

Channels are available for common ecommerce and marketing data structure such as orders, contacts, products, etc. 

Let's imagine that a developer creates workflows to receive orders from Shopify, eBay and Amazon. By using a standard model for these orders, the developer can write workflows without being concerned about how each of these sources formats their orders. Along the same lines, integrations are developed to work with these channels - for example, a SendGrid email receipt integration knows where to fund the email property in a provided order object.

### Primary channels

- *Order*: eCommerce orders
- *Product*: Store products
- *Category*: Product categories
- *Contact*: Custom contact
- *Lead*: Sales lead
- *Visitor*: Site visitor
- *Visit*: Visit entry for a visitor
- *Post*: Blog or article
- *Section*: Article category
- *Document*: Generic document

### Insight channels

In addition, certain channels have an associated insight table. For example, orders are summarized in the order insight channel which provides summary such as total sales per period, average order value etc... 

### Data visualization and manipulation

The dashboard UI provides both data tables to view channel info as well as relevant charts and graphs for insights. The data can also be exported to 3rd party analytics dashboard if desired.

