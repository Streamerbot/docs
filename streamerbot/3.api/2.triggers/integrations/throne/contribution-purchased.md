---
title: Contribution Purchased
description: Triggered when a contribution is purchased through the Throne integration
version: 1.0.5
variables:
  - name: throne.gifterLogin
    type: string
    description: The login of the gifter
    value: Lyfesaver74
  - name: throne.amount
    type: number
    description: The amount of the contribution, in cents
    value: 10000
  - name: throne.creatorId
    type: string
    description: The ID of the creator / recipient of the gift
    value: 'twitch:12345678'
  - name: throne.creatorLogin
    type: string
    description: The login of the creator / recipient of the gift
    value: twitchuser123
  - name: throne.message
    type: string
    description: The message attached to the gift
    value: 'Happy Birthday!'
  - name: throne.itemName
    type: string
    description: The name of the item purchased as a gift
    value: 'AirPods Max'
  - name: throne.itemThumbnailUrl
    type: string
    description: The URL of the thumbnail image for the item purchased as a gift
    value: 'https://m.media-amazon.com/images/I/81jqUPkIVRL._AC_SX522_.jpg'
  - name: throne.currency
    type: string
    description: The currency of the contribution amount
    value: 'USD'
  - name: throne.createdAt
    type: DateTime
    description: The timestamp when the gift was created
    value: '7/10/2026 3:01:00 PM'
---
