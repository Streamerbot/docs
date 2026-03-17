---
title: Kicks Gifted
description: Trigger for a Kicks Gifted event
version: 1.0.2
variables:
  - name: kicks.amount
    description: The amount of Kicks gifted
    type: int
    value: 42
  - name: kicks.name
    description: THe name of the gift reward
    type: string
    value: Kicks Gift
  - name: kicks.type
    description: The type of the gift reward
    type: string
    value: LEVEL_UP
  - name: kicks.tier
    description: The tier of the gift reward
    type: string
    value: MID
  - name: kicks.pinnedTimeSeconds
    description: The amount of seconds the gift is pinned in the chat
    type: int
    value: 600
  - name: kicks.createdAt
    description: The timestamp of when the gift was created
    type: string
    value: "1/1/0001 12:00:00 AM"
  - name: rawInput
    type: string
    description: The message receieved in chat
  - name: rawInputEscaped
    type: string
    description: The message escaped
  - name: rawInputUrlEncoded
    type: string
    description: The message URL encoded
  - name: input.count
    type: number
    description: The number of words in the message received
  - name: input#
    type: string
    description: The `#` word of the message entered, spaces are delimiters and variable names are 0 indexed, so `input0` would give the first word, `input1` would give the second, and so on
  - name: inputEscaped#
    type: string
    description: The indexed word escaped
  - name: inputUrlEncoded#
    type: string
    description: The indexed word URL encoded
commonVariables:
  - KickBroadcaster
  - KickUser
---
