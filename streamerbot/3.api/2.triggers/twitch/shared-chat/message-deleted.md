---
title: Shared Chat Message Deleted
description: Trigger for When a Twitch Chat Message Is Deleted in a Shared Chat
version: 0.2.5
twitchService: EventSub
variables:
  - name: targetMessageId
    type: string
    description: The unique identifier for the message that has been deleted
  - name: message
    type: string
    description: The content of the chat message that has been deleted
    value: My chat message
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
  - TwitchSharedChatSource
---