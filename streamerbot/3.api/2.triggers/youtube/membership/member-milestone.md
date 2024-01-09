---
title: Member Milestone
description: Trigger for YouTube member milestone events
variables:
  - name: messageId
    type: string
    description: The id of the member milestone event
  - name: publishedAt
    type: DateTime
    description: The time the member milestone event was published at
    value: 8/4/2023 10:56:06 AM
  - name: months
    type: number
    description: The total amount of months (rounded up) the viewer has been a member
    value: 6
  - name: levelName
    type: string
    description: The name of the Level at which the viewer is a member.
  - name: message
    type: string
    description: The message associated with the member milestone event
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---
