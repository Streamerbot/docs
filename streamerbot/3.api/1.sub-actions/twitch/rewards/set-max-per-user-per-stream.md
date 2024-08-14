---
title: Set Max per User Per Stream
description: Set's the maxmimum number of redeems possible per user per stream
version: 0.2.4
parameters:
  - name: Reward
    type: Select
    required: true
    description: Select the channel point reward
  - name: Redeems
    type: int
    required: true
    description: The number of redeems to set, this value can be a variable
  - name: Additive
    type: boolean
    required: true
    description: Whether or not the redeem value is to be added to the Reward's current max per user per stream
variables: []
csharpMethods:
  - UpdateRewardMaxPerUserPerStream
---
