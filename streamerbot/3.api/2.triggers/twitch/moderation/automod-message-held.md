---
title: AutoMod Message Held
description: Trigger for when an AutoMod message is held
version: 0.2.4
variables:
  - name: category
    type: string
    description: the automod category
    value: swearing, ableism, aggression, misogyny, namecalling, bullying
  - name: level
    type: int
    description: the automod level
    value: 1
  - name: heldAt
    type: datetime
    description: datetime of when the message has been held
    value: 28.06.2024 20:43:28
  - name: rawInput
    type: string
    description: the raw input of the message
    value: this is a test message
commonVariables:
  - TwitchUser
---
