---
title: Gift Purchase
description: Trigger for a FourthWall Gift being purchased
version: 0.2.3
variables:
  - name: fw.createdAt
    type: DateTime
    description: The DateTime of the purchased gift in UTC
  - name: fw.Id
    type: string
    description: Gift Order id
    value: giv_voWcDCtfQUygxpuYx1HtNg
  - name: fw.shopId
    type: string
    description: Shop id
    value: sh_7ad0c438-beda-4779-a885-0dc325a755c1
  - name: fw.friendly
    type: string
    description: Friendly id
    value: F2LGPYCV
  - name: fw.email
    type: string
    description: Supporter e-mail adress
    value: support@fourthwall.com
  - name: fw.username
    type: string
    description: Username
  - name: fw.statmessageus
    type: string
    description: Attached message
    value: message from supporter
  - name: fw.currency
    type: string
    description: Currency
    value: USD
  - name: fw.subtotal
    type: number
    description: Subtotal
    value: 10
  - name: fw.shipping
    type: number
    description: Shipping Cost
    value: 5
  - name: fw.tax
    type: number
    description: Tax Cost
    value: 1
  - name: fw.donation
    type: number
    description: Donation added to the order
    value: 3
  - name: fw.discount
    type: number
    description: Discount amount that was applied
    value: 2
  - name: fw.total
    type: number
    description: Order total amount
    value: 17
  - name: fw.offer.id
    type: string
    description: Gift offer id
    value: b2c201d3-8104-4b2a-b2c9-1f6b335b650a
  - name: fw.offer.name
    type: string
    description: Gift product name
    value: New T-shirt
  - name: fw.offer.slug
    type: string
    description: Gift product slug
    value: new-t-shirt
  - name: fw.offer.description
    type: string
    description: Gift product description
  - name: fw.offer.imageUrl
    type: string
    description: Gift product image url
    value: https://cdn.staging.fourthwall.com/customization/sh_7ad0c438-beda-4779-a885-0dc325a755c1/5a125858-0e0c-4099-996f-db61cbd62f8e.jpeg
  - name: fw.gifts[0].status
    type: string
    description: Status of gift
    value: REDEEMED
  - name: fw.gifts[0].id
    type: string
    description: Gift id
    value: gft_EdJvIXu3SEiXe_QkPavHSA
  - name: fw.gifts[0].orderId
    type: string
    description: Gift order id
    value: 7b83a86f-9221-4416-b739-ef88870f999b
  - name: fw.gifts[0].orderFriendlyId
    type: string
    description: Friendly order id
    value: F2LGPYCV
  - name: fw.gifts[0].winner
    type: string
    description: Gift winner name
    value: supporter-username
  - name: fw.gifts[1].status
    type: string
    description: Gift status
    value: AVAILABLE
  - name: fw.gifts[1].id
    type: string
    description: Gift id
    value: gft_EdJvIXu3SEiXe_QkPavHSA
  - name: fw.gifts[1].winner
    type: string
    description: Winner name
    value: winner-1
  - name: fw.gifts[2].status
    type: string
    description: Gift status
    value: CANCELLED
  - name: fw.gifts[2].id
    type: string
    description: Gift id
    value: gft_EdJvIXu3SEiXe_QkPavHSA
  - name: fw.gifts[2].winner
    type: string
    description: Winner name
    value: winner-2
  - name: fw.gifts[3].status
    type: string
    description: Gift status
    value: 'CHANGED_TO_PROMOTION'
  - name: fw.gifts[3].id
    type: string
    description: Gift id
    value: gft_EdJvIXu3SEiXe_QkPavHSA
  - name: fw.gifts[3].promotionId
    type: string
    description: Gift promotion id
    value: 'prm_EdJvIXu3SEiXe_QkPavHSA'
  - name: fw.gifts[3].winner
    type: string
    description: Winner name
    value: winner-3
---
