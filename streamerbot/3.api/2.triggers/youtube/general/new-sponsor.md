---
title: New Sponsor
description: Trigger for YouTube sponsor events
variables:
  - name: messageId
    type: string
    description: The id of the sponsor event
  - name: publishedAt
    type: DateTime
    description: The time the sponsor event was published at
    value: 8/4/2023 10:56:06 AM
  - name: isUpgrade
    type: boolean
    description: Indicates whether the viewer just upgraded from a lower level
    value: True
  - name: levelName
    type: string
    description: The name of the Level at which the viewer is a member
commonVariables:
  - YouTubeUser
  - YouTubeBroadcast
  - YouTubeBroadcaster
---
