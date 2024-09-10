---
title: Send Message
description: Send a Twitch chat message
parameters:
  - name: Message
    type: Text
    required: true
    description: |
      Enter the message contents
  - name: Send using bot account
    version: 0.2.5
    type: Toggle
    default: Unchecked
    required: true
    description: |
      - [x] Send the reply using your **Twitch Bot** account
      - [ ] Send the reply using your **Twitch Broadcaster** account
  - name: Fallback to Broadcaster
    version: 0.2.5
    type: Toggle
    default: Unchecked
    required: true
    description: |
      - [x] If `Send using Bot account` is **checked**, it will attempt to send reply as Twitch Bot account and, if unable, then send as Twitch Broadcaster.
      - [ ] If `Send using Bot account` is **unchecked**, it will attempt to send reply as Twitch Bot account and, if unable, then do **nothing** (i.e. the Twitch Bot account is not logged in.
variables: []
csharpMethods:
  - SendMessage
---
