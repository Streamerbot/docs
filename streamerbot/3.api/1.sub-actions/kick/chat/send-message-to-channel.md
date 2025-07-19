---
title: Kick Message
description: Send a Kick chat message
parameters:
  - name: Message
    type: Text
    required: true
    description: |
      Enter the message contents
  - name: Send using bot account
    type: Toggle
    default: Unchecked
    description: |
      - [x] Send the reply using your **Kick Bot** account
      - [ ] Send the reply using your **Kick Broadcaster** account
  - name: Fallback to Broadcaster
    type: Toggle
    default: Unchecked
    description: |
      - [x] If `Send using Bot account` is **checked**, it will attempt to send reply as Kick Bot account and, if unable, then send as Kick Broadcaster.
      - [ ] If `Send using Bot account` is **unchecked**, it will attempt to send reply as Kick Bot account and, if unable, then do **nothing** (i.e. the Kick Bot account is not logged in.
variables: []
csharpMethods:
  - SendKickMessage
---