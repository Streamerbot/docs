---
title: Membership Gift
description: Trigger for YouTube gift memberships
variables:
  - name: id
    type: string
    description: The ID of the memberships gift event
  - name: count
    type: int
    description: The number of memberships gifted
    value: 12
  - name: tier
    type: string
    description: The tier of memberships gifted
commonVariables:
  - YouTubeUser
  - YouTubeBroadcast
  - YouTubeBroadcaster
---
