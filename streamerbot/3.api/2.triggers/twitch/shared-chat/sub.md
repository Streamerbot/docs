---
title: Shared Sub
description: Triggered When a User Subscribes in a Shared Chat
twitchService: EventSub
version: 0.2.5
variables:
  - name: tier
    type: string
    description: The subscription tier<br>`prime`, `tier 1`, `tier 2`, `tier 3`
    value: tier 1
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
  - TwitchChat
  - TwitchSharedChatSource
---
