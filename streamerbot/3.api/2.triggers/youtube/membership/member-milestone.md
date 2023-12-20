---
title: Member Milestone
description: Trigger for YouTube member milestone events
variables:
  - name: messageId
    description: The id of the member milestone event
  - name: publishedAt
    description: The time the member milestone event was published at
  - name: months
    description: The total amount of months (rounded up) the viewer has been a member
  - name: levelName
    description: The name of the Level at which the viewer is a member.
  - name: message
    description: The message associated with the member milestone event
commonVariables:
  - YouTubeBroadcaster
---