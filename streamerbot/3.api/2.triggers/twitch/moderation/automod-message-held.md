---
title: AutoMod Message Held
description: Trigger for when an AutoMod message is held
version: 0.2.4
variables:
  - name: messageId
    type: string
    description: the message ID
    value: 2521b4be-733e-4dfe-b4c2-0b72e2fdc205
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
  - name: input[i]
    type: string
    description: the rawInput string stripped by spaces, starting with input0 for the first word, input1 for the second etc.
    value: this
commonVariables:
  - TwitchUser
---
