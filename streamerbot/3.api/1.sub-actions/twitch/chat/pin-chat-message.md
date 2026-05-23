---
name: Pin Chat Message
title: Pin Chat Message
description: Pins the provided message
version: 1.0.5
parameters:
  - name: Message Id
    type: Text
    required: true
    description: |
      Enter the ID of the message to pin
  - name: Duration
    type: Text
    required: false
    description: |
        The duration to pin the chat message for.
        - `null` for the pin to last till the end of the stream
        - between `30` and `1800` - duration in seconds
csharpmethods:
    - TwitchChatPinMessage
---
