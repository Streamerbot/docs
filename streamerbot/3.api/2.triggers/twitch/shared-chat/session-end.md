---
title: Twitch Shared Chat Session End
description: Trigger for When a Twitch Shared Chat Session Ends
version: 0.2.5
twitchService: Chat Client
variables:
  - name: host.userId
    type: string
    value: 519435394
    description: Twitch user ID of the host
  - name: host.userLogin
    type: string
    value: reallycoolhost
    description: Twith login name of the host  
  - name: host.userName
    type: string
    value: ReallyCoolHost
    description: Twith user name of the host
  - name: host.isSubscribed
    type: boolean
    value: False
    description: Returns `True` if host is subscribed to the Twitch Broadcaster  
  - name: host.isModerator
    type: boolean
    value: False
    description: Returns `True` if host is a moderator in the Twitch Broadcaster's channel
  - name: host.isVip
    type: boolean
    value: True
    description: Returns `False` if host is not VIP in the Twitch Broadcaster's channel
commonVariables:
  - TwitchChat
  - TwitchUser
---
