---
title: Chat Message
description: Trigger for a Twitch Chat Message
version: 0.0.50
twitchService: Chat Client
variables:
  - name: internal
    type: boolean
    description: |
      If message was sent via Streamer.bot sub-action or C#

      Messages from Streamer.bot Chat are not considered as internal since `0.2.5`
    value: True / False
commonVariables:
  - TwitchUser
  - TwitchChat
---
