---
title: Chat Message
description: Trigger for a Twitch Chat Message
version: 0.0.50
twitchService: Chat Client
variables:
  - name: internal
    type: boolean
    description: Was the message sent from Streamer.bot?
    value: True
commonVariables:
  - TwitchUser
  - TwitchChat
---
