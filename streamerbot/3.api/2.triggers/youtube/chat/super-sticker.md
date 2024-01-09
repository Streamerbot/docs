---
title: Super Sticker
description: Trigger for YouTube Super Sticker events
variables:
  - name: messageId
    type: string
    description: The id of the super sticker event
  - name: publishedAt
    type: DateTime
    description: The time the super sticker event was published at
    value: 8/4/2023 10:56:06 AM
  - name: tier
    type: number
    description: The tier for the paid message
  - name: amount
    type: string
    description: The amount of donated money from the super sticker
    value: $1.00
  - name: microAmount
    type: number
    description: The purchase amount, in micros of the purchase currency
    value: $1 > 1000000
  - name: currencyCode
    type: string
    description: The currency in which the purchase was made. The value is an ISO 4217 currency code.
    value: EUR
  - name: stickerId
    type: string
    description: A unique ID that identifies the sticker image.
  - name: stickerAltText
    type: string
    description: A text string that describes the sticker.
  - name: stickerLanguage
    type: string
    description: The language of the `stickerAltText`
    value: EN
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---