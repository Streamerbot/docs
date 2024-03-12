---
title: Reply to Message
description: Send a reply to a specific Twitch chat message
parameters:
  - name: Preferred Account
    type: Select
    default: Bot
    required: true
    description: |
      - `Broadcaster` - Send the reply using your **Twitch Broadcaster** account
      - `Bot` - Send the reply using your **Twitch Bot** account
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
variables: []
csharpMethods:
  - TwitchReplyToMessage
---
