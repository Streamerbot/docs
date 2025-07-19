---
title: Kick Reply to Message
description: Send a reply to a specific Kick chat message
parameters:
  - name: Reply Id
    type: Text
    default: '%msgId%'
    required: true
    description: |
      Enter the unique ID of the message to reply to

      ::tip
      All triggers that contain the `Kick Chat` variables, will populate the `%msgId%`{lang=cs} variable
      ::
  - name: Message
    type: Text
    required: true
    description: |
      Enter the message contents
  - name: Send using bot account
    type: Toggle
    default: false
    description: |
      - [x] Send the reply using your **Kick Bot** account
      - [ ] Send the reply using your **Kick Broadcaster** account
  - name: Fallback to Broadcaster
    type: Toggle
    default: false
    description: |
      - [x] If `Send using Bot account` is **checked**, it will attempt to send reply as Kick Bot account and, if unable, then send as Kick Broadcaster.
      - [ ] If `Send using Bot account` is **unchecked**, it will attempt to send reply as Kick Bot account and, if unable, then do **nothing** (i.e. the Kick Bot account is not logged in.
variables: []
csharpMethods:
  - KickReplyToMessage
---
