---
title: First Words
description: Trigger for a YouTube chatter's first message
variables:
  - name: messageId
    type: string
    description: The id of the message
  - name: message
    type: string
    description: The message sent to the chat
  - name: publishedAt
    type: DateTime
    description: The time the message was published at
    value: 8/4/2023 10:56:06 AM
  - name: rawInput
    type: string
    description: The raw message sent to the chat
  - name: rawInputEscaped
    type: string
    description: The raw message sent to the chat escaped
  - name: "input#"
    type: string
    description: "Each word from `rawInput`. `input0`, `input1`, and so on..."
  - name: input#Escaped
    type: string
    description: "Each word from `rawInput`, escaped. `input0Escaped`, `input1Escaped`, and so on..."
  - name: userIsSponsor
    type: boolean
    description: Indicates whether the viewer is a current channel member or not
    value: True
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---
