---
title: Super Sticker
description: Trigger for YouTube Super Sticker events
variables:
  - name: messageId
    description: The id of the super sticker event
  - name: publishedAt
    description: The time the super sticker event was published at
  - name: tier
    description: The tier for the paid message
  - name: amount
    description: A string, like $1.00, that contains the purchase amount and currency. The string is intended to be displayed to the user.
  - name: microAmount
    description: The purchase amount, in micros of the purchase currency. For example, if the purchase amount is one dollar, the value is 1000000.
  - name: currencyCode
    description: The currency in which the purchase was made. The value is an ISO 4217 currency code.
  - name: stickerId
    description: A unique ID that identifies the sticker image.
  - name: stickerAltText
    description: A text string that describes the sticker.
  - name: stickerLanguage
    description: The language of the `stickerAltText`
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---