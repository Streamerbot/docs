---
title: Tip
description: Trigger for a StreamElements Tip
version: 0.2.1
parameters:
  - name: Range
variables:
  - name: tipUsername
    type: string
    description: Username of the user as provided by StreamElements (may not be from Twitch)
  - name: tipAvatar
    type: string
    description: The URL of the user's avatar
  - name: tipAmount
    type: number
    description: The amount of the tip
    value: 5
  - name: tipCurrency
    type: string
    description: The 3 letter payment currency code
    value: EUR
  - name: tipMessage
    type: string
    description: The tip message that the user may has included
    value: My tip message
---
