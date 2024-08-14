---
title: Super Chat
description: Trigger for YouTube Super Chat events
variables:
  - name: messageId
    type: string
    description: The id of the super chat event
  - name: message
    type: string
    description: The message of the super chat event
    value: Here you go!
  - name: publishedAt
    type: DateTime
    description: The time the super chat event was published at
    value: 8/4/2023 10:56:06 AM
  - name: tier
    type: number
    description: The tier for the paid message
  - name: amount
    type: string
    description: The purchase amount, in user-friendly text
    value: $1.00
  - name: microAmount
    type: number
    description: The purchase amount, in micros of the purchase currency.
    value: 1000000
  - name: currencyCode
    type: string
    description: The ISO 4217 currency code for the purchase
    value: USD
commonVariables:
  - YouTubeUser
  - YouTubeBroadcast
  - YouTubeBroadcaster
---

