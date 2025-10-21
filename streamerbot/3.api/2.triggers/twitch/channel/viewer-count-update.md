---
title: Viewer Count Update
description: Trigger for when your Twitch viewer count updates
version: 0.2.0
twitchService: EventSub
parameters:
  - name: Range
    import: common/range
variables:
  - name: viewerCount
    type: number
    description: The new Twitch viewer count
    value: 187
commonVariables:
  - TwitchBroadcaster
---
