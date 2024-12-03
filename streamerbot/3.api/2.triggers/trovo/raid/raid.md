---
title: Raid
description: Trigger for a Trovo raid
parameters:
  - name: Range
variables:
  - name: raid.sentAt
    type: DateTime
    description: The timestamp the raid was sent
  - name: raid.raiderCount
    type: number
    description: The amount of users that participated in the raid
commonVariables:
  - TrovoUser
---
