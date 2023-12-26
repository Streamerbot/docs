---
title: Announcement
description: Trigger for a Twitch Announcement
version: 0.1.9
twitchService: Chat Client
variables:
  - name: announceColor
    type: string
    description: The color of the announcement<br>`DEFAULT`, `BLUE`, `RED`, `ORANGE`, `PURPLE`
    value: BLUE
commonVariables:
  - TwitchUser
  - TwitchChat
---