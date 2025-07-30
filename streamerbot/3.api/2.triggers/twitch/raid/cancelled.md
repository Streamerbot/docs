---
title: Raid Cancelled
description: Trigger for when a Twitch Raid from your channel to another channel is Cancelled
version: 0.0.36
twitchService: EventSub
variables:
  - name: raidUser
    type: string
    description: The raider's username
    value: TwitchUser123
  - name: raidUserName
    type: string
    description: The raider's login name
    value: twitchuser123
  - name: raidUserId
    type: string
    description: The raider's user id
    value: 718933593
  - name: raidUserProfileImageURL
    type: string
    description: The raider's profile image URL
  - name: raidUserProfileImageEscaped
    type: string
    description: The raider's profile image URL escaped
commonVariables:
  - TwitchBroadcaster
---
