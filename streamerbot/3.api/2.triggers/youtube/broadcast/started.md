---
title: Broadcast Started
description: Trigger for YouTube broadcast starting
variables:
  - name: title
    type: string
    description: The title of the broadcast
    value: My Cool Stream
  - name: description
    type: string
    description: The description of the broadcast
    value: Check out what we're doing on My Cool Stream!
  - name: publishedAt
    type: DateTime
    description: The time the broadcast was started at
    value: 8/4/2023 10:56:06 AM
  - name: broadcastId
    type: string
    description: The unique ID of the broadcast
commonVariables:
  - YouTubeBroadcaster
---