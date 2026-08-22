---
title: Gift Purchased
description: Triggered when a gift is purchased through the Throne integration
version: 1.0.5
variables:
  - name: throne.gifterLogin
    type: string
    description: The login of the gifter
    value: Lyfesaver74
  - name: throne.isSurpriseGift
    type: boolean
    description: Indicates if the gift is a surprise
    value: False
  - name: throne.price
    type: number
    description: The price of the gift, in cents
    value: 10000
  - name: throne.creatorId
    type: string
    description: The ID of the creator / recipient of the gift
    value: "twitch:12345678"
  - name: throne.creatorLogin
    type: string
    description: The login of the creator / recipient of the gift
    value: twitchuser123
  - name: throne.message
    type: string
    description: The message attached to the gift
    value: "Happy Birthday!"
  - name: throne.itemName
    type: string
    description: The name of the item purchased as a gift
    value: "AirPods Max"
  - name: throne.itemThumbnailUrl
    type: string
    description: The URL of the thumbnail image for the item purchased as a gift
    value: "https://m.media-amazon.com/images/I/81jqUPkIVRL._AC_SX522_.jpg"
  - name: throne.currency
    type: string
    description: The currency of the gift price
    value: "USD"
  - name: throne.createdAt
    type: DateTime
    description: The timestamp when the gift was created
    value: "7/10/2026 3:01:00 PM"
---
