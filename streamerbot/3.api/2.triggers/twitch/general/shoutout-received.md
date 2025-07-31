---
title: Shoutout Received
description: Trigger for when a Twitch Shoutout is Received
version: 0.1.17
twitchService: Chat Client
variables:
  - name: viewerCount
    type: number
    description: The viewer count from the user that created the shoutout
    value: 200
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---