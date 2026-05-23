---
title: User Timed Out
description: Trigger for YouTube user timedout events
version: 1.0.5
parameters:
  - name: Range
    import: common/range
variables:
  - name: banDuration
    type: number
    description: The duration of the ban in seconds.
    value: 60
commonVariables:
  - YouTubeUser
  - YouTubeBroadcast
  - YouTubeBroadcaster
---
