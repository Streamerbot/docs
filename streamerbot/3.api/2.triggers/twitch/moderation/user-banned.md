---
title: User Banned
description: Trigger for when a Twitch User is Banned
twitchService: PubSub
variables:
  - name: user
    type: string
    description: The user who was banned<br>*This will only be populated if the user has been present in chat*
    value: TwitchUser123
  - name: createdAt
    type: DateTime
    description: The timestamp when the ban was created
    value: 8/4/2023 10:56:06 AM
  - name: createdById
    type: string
    description: The Twitch user id from who created the ban
  - name: createdByUsername
    type: string
    description: The Twitch user name from who created the ban
    value: twitchuser123
  - name: createdByDisplayName
    type: string
    description: The Twitch display name from who created the ban
    value: TwitchUser123
  - name: reason
    type: string
    description: The reason for the ban
    value: My ban reason
---