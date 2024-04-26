---
title: Product Updated
description: Trigger for a FourthWall product being updated
version: 0.2.3
variables:
  - name: fw.createdAt
    type: DateTime
    description: DateTime of when the product was created
  - name: fw.updatedAt
    type: DateTime
    description: DateTime of when the product was updated
  - name: fw.productId
    type: string
    description: Product Id
    value: cc5d40e3-9f67-4e5d-8530-1d3f738ca915
  - name: fw.shopId
    type: string
    description: Id of the shop
    value: sh_7ad0c438-beda-4779-a885-0dc325a755c1
  - name: fw.name
    type: string
    description: Name
    value: Updated T-shirt
  - name: fw.description
    type: string
    description: Description
    value: desc
  - name: fw.slug
    type: string
    description: Slug name
    value: new-t-shirt
  - name: fw.state
    type: string
    description: State
    value: AVAILABLE
  - name: fw.images[#]
    type: string
    description: Image urls
    value: https://cdn.staging.fourthwall.com/customization/sh_7ad0c438-beda-4779-a885-0dc325a755c1/5a125858-0e0c-4099-996f-db61cbd62f8e.jpeg
  - name: fw.variants[#].id
    type: string
    description: Id
    value: e3c12d65-a3aa-417e-a289-dabf71a87194
  - name: fw.variants[#].name
    type: string
    description: Name
    value: New T-shirt
  - name: fw.variants[#].sku
    type: string
    description: SKU
    value: Z3YD-8CTV00S
  - name: fw.variants[#].image
    type: string
    description: Image url
    value: https://cdn.staging.fourthwall.com/customization/sh_7ad0c438-beda-4779-a885-0dc325a755c1/5a125858-0e0c-4099-996f-db61cbd62f8e.jpeg
  - name: fw.variants[#].unitPrice
    type: number
    description: Unit price
    value: 5
  - name: fw.variants[#].currencyCode
    type: string
    description: Currency code
    value: USD
  - name: fw.variants[0].stockType
    type: string
    description: Stock Type
    value: UNLIMITED
  - name: fw.variants[#].attributes.description
    type: string
    description: Description
    value: White, S
  - name: fw.variants[#].attributes.color
    type: string
    description: Color
    value: White
  - name: fw.variants[#].attributes.colorSwatch
    type: string
    description: Hex color
    value: '#FFFFFF'
  - name: fw.variants[#].attributes.size
    type: string
    description: Size
    value: S
  - name: fw.variants[#].attributes.weight
    type: string
    description: Weight
    value: 1
  - name: fw.variants[#].stock
    type: string
    description: Current stock
    value: 0
---
