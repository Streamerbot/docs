---
title: Warned User
description: Trigger for when a Twitch user is warned
version: 0.2.4
twitchService: EventSub
variables:
  - name: moderator.userName
    type: string
    description: display name of the moderator who did the warning
    value: Lyfesaver74
  - name: moderator.login
    type: string
    description: login name of the moderator who did the warning
    value: lyfesaver74
  - name: moderator.id
    type: string
    description: display name of the moderator who did the warning
    value: 161545467
  - name: reason
    type: string
    description: the reason specified in the warning
    value: spam
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---
