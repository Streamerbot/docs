---
title: Raid Start
description: Trigger for when a Twitch Raid from your channel to another channel is Started
version: 0.0.33
twitchService: PubSub
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
  - name: raidUserProfileImageURL
    type: string
    description: The raider's profile image URL
  - name: raidUserProfileImageEscaped
    type: string
    description: The raider's profile image URL escaped
---