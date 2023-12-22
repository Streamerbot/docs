---
title: First Words
description: Trigger for a YouTube chatter's first message
variables:
  - name: messageId
    description: The id of the message
  - name: message
    description: The message sent to the chat
  - name: publishedAt
    description: The time the message was published at
  - name: rawInput
    description: The raw message sent to the chat
  - name: rawInputEscaped
    description: The raw message sent to the chat escaped
  - name: "input#"
    description: "Each word from `rawInput`. `input0`, `input1`, and so on..."
  - name: input#Escaped
    description: "Each word from `rawInput`, escaped. `input0Escaped`, `input1Escaped`, and so on..."
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---