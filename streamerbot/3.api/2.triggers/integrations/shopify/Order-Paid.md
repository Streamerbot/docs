---
title: Order Paid
description: Trigger for when a Shopify Order is Paid
version: 0.1.14
variables:
  - name: shopify.created_at
    type: DateTime
    description: The timestamp the order was created
    value: 8/4/2023 10:56:06 AM
  - name: shopify.event
    type: string
    description: The event name
    value: orders/create
  - name: shopify.id
    type: string
    description: The shopify id
  - name: shopify.email
    type: string
    description: The email of the customer
    value: jon@doe.ca
  - name: shopify.closed_at
    type: DateTime
    description: The timestamp that the store closed
    value: 8/4/2023 10:56:06 AM
  - name: shopify.updated_at
    type: DateTime
    description: The timestamp that the store was last updated
    value: 8/4/2023 10:56:06 AM
  - name: shopify.number
    type: string
    description: The order number
  - name: shopify.note
    type: string
    description: The note that the customer left
  - name: shopify.total_price
    type: number
    description: The total price of the order
    value: 254.98
  - name: shopify.subtotal_price
    type: number
    description: The subtotal price of the order
    value: 244.98
  - name: shopify.currency
    type: string
    description: The 3 letter currency
    value: EUR
  - name: shopify.financial_status
    type: string
    description: The financial status
    value: voided
  - name: shopify.confirmed
    type: boolean
    description: The confirmed status
    value: True
  - name: shopify.total_discounts
    type: number
    description: The total amount of discounts from the order
    value: 5.00
  - name: shopify.total_line_items_price
    type: number
    description: The total price
    value: 249.98
  - name: shopify.buyer_accepts_marketing
    type: boolean
    description: If the customer accepts marketing
    value: True
  - name: shopify.name
    type: string
    description: The name of the customer
  - name: shopify.referring_site
    type: string
    description: The referring site
  - name: shopify.landing_site
    type: string
    description: The landing site
  - name: shopify.total_price_usd
    type: number
    description: The total price in USD
  - name: shopify.order_number
    type: string
    description: The order number
  - name: shopify.line_items[#].id
    type: string
    description: The item id
  - name: shopify.line_items[#].variant_id
    type: string
    description: The item variant id
  - name: shopify.line_items[#].title
    type: string
    description: The item's title
    value: Aviator sunglasses
  - name: shopify.line_items[#].quantity
    type: number
    description: The quantity of this item
  - name: shopify.line_items[#].sku
    type: string
    description: The stock keeping unit
    value: SKU2006-001
  - name: shopify.line_items[#].variant_title
    type: string
    description: The item variant title
  - name: shopify.line_items[#].vendor
    type: string
    description: The seller of this item
  - name: shopify.line_items[#].fulfillment_service
    type: string
    description: The fulfillment service e.g. `manual`
  - name: shopify.line_items[#].product_id
    type: string
    description: The product's id of this item
  - name: shopify.line_items[#].requires_shipping
    type: boolean
    description: If this item requires shipping
    value: True
  - name: shopify.line_items[#].taxable
    type: boolean
    description: If this item is taxable
    value: True
  - name: shopify.line_items[#].gift_card
    type: boolean
    description: If this item is a gift card
    value: True
  - name: shopify.line_items[#].name
    type: string
    description: The item's name
    value: Aviator sunglasses
  - name: shopify.line_items[#].variant_inventory_management
    type: string
    description: The inventory management of this item
  - name: shopify.line_items[#].product_exists
    type: boolean
    description: If the products exists
    value: True
  - name: shopify.line_items[#].fulfillable_quantity
    type: number
    description: The quantity left of this item
    value: 5
  - name: shopify.line_items[#].grams
    type: number
    description: The amount of metric grams in this item
    value: 100
  - name: shopify.line_items[#].price
    type: number
    description: The price of this item
    value: 89.99
  - name: shopify.line_items[#].total_discount
    type: number
    description: The total discount on this item
    value: 0.00
  - name: shopify.line_items[#].fulfillment_status
    type: string
    description: The fulfillment status of this item
  - name: shopify.line_items[#].price_set.shop_money.amount
    type: number
    description: The shop money amount of this item
    value: 89.99
  - name: shopify.line_items[#].price_set.shop_money.currency_code
    type: string
    description: The shop money currency code of this item
    value: EUR
  - name: shopify.line_items[#].price_set.presentment_money.amount
    type: number
    description: The presentment money of this item
    value: 89.99
  - name: shopify.line_items[#].price_set.presentment_money.currency_code
    type: string
    description: The presentment currency code of this item
    value: EUR
  - name: shopify.line_items[#].total_discount_set.shop_money.amount
    type: number
    description: The total discount amount of this item
    value: 0.00
  - name: shopify.line_items[#].total_discount_set.shop_money.currency_code
    type: string
    description: The total discount currency code of this item
    value: EUR
  - name: shopify.line_items[#].total_discount_set.presentment_money.amount
    type: number
    description: The total discount presentment money of this item
    value: 0.00
  - name: shopify.line_items[#].total_discount_set.presentment_money.currency_code
    type: string
    description: The total discount presentment currency code of this item
    value: EUR
  - name: shopify.line_items[#].admin_graphql_api_id
    type: string
    description: The admin GraphQL API ID of this item
    value: gid://shopify/LineItem/<numeric id>
  - name: _json
    type: string
    description: The variables in JSON for C# usage.
---