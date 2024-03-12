---
description: Send a reply to a specific Twitch chat message
parameters:
  - name: message
    value: '"Hello, world!"'
    description: Enter the message contents
  - name: replyId
    value: 'args["msgId"]'
    description: Enter the unique ID of the message to reply to
  - name: bot
    value: true
    description: |
      - `true`{lang=cs} - Send the reply using your **Twitch Bot** account
      - `false`{lang=cs} - Send the reply using your **Twitch Broadcaster** account
---