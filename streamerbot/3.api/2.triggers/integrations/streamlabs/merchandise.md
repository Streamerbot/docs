---
title: Merchandise
description: Trigger for when a Merchandise item is bought in Streamlabs
variables:
  - name: merchandiseFrom
    type: string
    description: The username of the user as provided by Streamlabs (may not be from Twitch)
  - name: merchandiseMessage
    type: string
    description: The message that the user may has included
    value: My merchandise message
  - name: merchandiseProduct
    type: string
    description: The product that was purchased
  - name: merchandiseImageUrl
    type: string
    description: The URL to the image of the product
  - name: merchandiseImageEscaped
    type: string
    description: The URL to the image of the product with escaped characters
---