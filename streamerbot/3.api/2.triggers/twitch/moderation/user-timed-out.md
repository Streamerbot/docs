---
title: User Timed Out
description: Trigger for when a Twitch User is Timed Out
twitchService: PubSub
variables:
  - name: user
    type: string
    description: The user who was timed out<br>*This will only be populated if the user has been present in chat*
    value: TwitchUser123
  - name: createdAt
    type: DateTime
    description: The timestamp when the timeout was created
    value: 8/4/2023 10:56:06 AM
  - name: createdById
    type: string
    description: The Twitch user id from who created the timeout
  - name: createdByUsername
    type: string
    description: The Twitch user name from who created the timeout
    value: twitchuser123
  - name: createdByDisplayName
    type: string
    description: The Twitch display name from who created the timeout
    value: TwitchUser123
  - name: reason
    type: string
    description: The reason for the timeout
    value: My timeout reason
  - name: duration
    type: number
    description: The duration of the timeout
    value: 300
---