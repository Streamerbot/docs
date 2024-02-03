---
title: User Banned
description: Trigger for YouTube user banned events
variables:
  - name: banType
    type: string
    description: The type of the ban
    example: temporary, permanent
  - name: banDuration
    type: number
    description: The duration of the ban in seconds. If permanent it will be 0
    example: 60  
commonVariables:
  - YouTubeUser
  - YouTubeBroadcaster
---
