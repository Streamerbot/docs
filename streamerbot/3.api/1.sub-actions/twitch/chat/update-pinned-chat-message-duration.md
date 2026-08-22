---
title: Update Pinned Chat Message Duration
description: Modify the duration of the pinned message in Twitch chat
version: 1.0.5
- name: Message Id
    type: Text
    required: true
    description: |
      Enter the ID of the message to modify
  - name: Duration
    type: Number
    required: false
    description: |
        The duration to pin the chat message for.
        - `null` for the pin to last till the end of the stream
        - between `30` and `1800` - duration in seconds
csharpmethods:
  - TwitchUpdatePinnedChatMessageDuration
---

:wip
