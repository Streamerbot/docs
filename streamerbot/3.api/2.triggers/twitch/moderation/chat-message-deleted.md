---
title: Chat Message Deleted
description: Trigger for when a Twitch Chat Message is Deleted
version: 0.1.18
twitchService: EventSub
variables:
  - name: targetMessageId
    type: string
    description: The unique identifier for the message that has been deleted
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---