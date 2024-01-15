---
title: Merch
description: Trigger for when a Merch item is bought in StreamElements
version: 0.2.1
variables:
  - name: merchUsername
    type: string
    description: Username of the user as provided by StreamElements (may not be from Twitch)
  - name: merchAvatar
    type: string
    description: The URL of the user's avatar
  - name: merchAmount
    type: number
    description: The amount of the purchase
    value: 45
  - name: merchCurrency
    type: string
    description: The 3 letter payment currency code
    value: EUR
  - name: merchMessage
    type: string
    description: The message that the user may has included
    value: My merch message
  - name: merchQuantity
    type: number
    description: The total number of items purchased
    value: 3
  - name: merchItems
    type: number
    description: The number of distinct items purchased
    value: 2
  - name: merchItem#.name
    type: string
    description: Name of the item purchased
  - name: merchItem#.price
    type: number
    description: Price of the item purchased
    value: 15
  - name: merchItem#.quantity
    type: number
    description: How many of the item was purchased
    value: 2
---