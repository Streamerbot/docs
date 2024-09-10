---
title: Reply to Message
description: Send a reply to a specific Twitch chat message
parameters:
  - name: Reply Id
    type: Text
    default: '%msgId%'
    required: true
    description: |
      Enter the unique ID of the message to reply to

      ::tip
      All triggers that contain the `Twitch Chat` variables, will populate the `%msgId%`{lang=cs} variable
      ::
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
      - `Checked` - Send the reply using your **Twitch Bot** account
      - `Unchecked` - Send the reply using your **Twitch Broadcaster** account
  - name: Fallback to Broadcaster
    version: 0.2.5
    type: Toggle
    default: Unchecked
    required: true
    description: |
      - `Checked` - (If `Send using Bot account` is **checked**), it will attempt to send reply as Twitch Bot account and if unable, then send as Twitch Broadcaster.
      - `Unchecked` - (If `Send using Bot account` is **unchecked**), it will attempt to send reply as Twitch Bot account and if unable, then do **nothing** (i.e. the Twitch Bot account is not logged in.
variables: []
csharpMethods:
  - TwitchReplyToMessage
---
