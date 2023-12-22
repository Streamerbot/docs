---
title: Message
description: Trigger for incoming YouTube chat messages
variables:
  - name: messageId
    type: string
    description: The ID of the message
  - name: message
    type: string
    description: The message contents
    value: Hello, world!
  - name: publishedAt
    type: DateTime
    description: The time the message was sent at
    value: 8/4/2023 10:56:06 AM
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---