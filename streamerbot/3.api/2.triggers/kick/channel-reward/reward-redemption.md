---
title: Reward Redemption
description: Trigger for a Kick Channel Reward Redemption
version: 1.0.2
variables:
  - name: reward.id
    description: The ID of the reward that was redeemed
    type: string
    value: "01KKYB2KFPMSBMAGYHWQRH2SV0"
  - name: reward.title
    description: The title of the reward that was redeemed
    type: string
    value: "My Reward"
  - name: reward.description
    description: The description of the reward that was redeemed
    type: string
    value: "This is my cool reward"
  - name: reward.cost
    description: The cost of the reward that was redeemed
    type: int
    value: 100
  - name: reward.backgroundColor
    description: The background color of the reward that was redeemed, in hex format
    type: string
    value: "#e5e5e5"
  - name: reward.skipsQueue
    description: Whether the reward that was redeemed skips the queue
    type: bool
    value: false
  - name: reward.requiresUserInput
    description: Whether the reward that was redeemed requires user input
    type: bool
    value: true
  - name: rawInput
    type: string
    description: The raw user input for the reward redemption, if applicable
    value: "This is my reward input"
  - name: rawInputEscaped
    type: string
    description: The raw user input for the reward redemption, escaped
    value: "This is my reward input"
  - name: rawInputUrlEncoded
    type: string
    description: The raw user input for the reward redemption, URL encoded
    value: "This%20is%20my%20reward%20input"
commonVariables:
  - KickBroadcaster
  - KickUser
---
