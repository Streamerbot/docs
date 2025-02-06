---
title: Raid Send
description: Triggers when the viewers successfully leave the broadcasters chat and arrive in raidUser's stream.
version: 0.0.36
twitchService: EventSub
variables:
  - name: raidUser
    type: string
    description: Display name of user that is being raided
    value: TwitchUser123
  - name: raidUserName
    type: string
    description: Login name of user that is being raided
    value: twitchuser123
  - name: raidUserId
    type: string
    description: User id of user that is being raided
    value: 718933593
  - name: raidUserProfileImageURL
    type: string
    description: Profile image URL of user that is being raided
  - name: raidUserProfileImageEscaped
    type: string
    description: Profile image URL escaped of user that is being raided
  - name: viewers
    type: number
    description: Amount of viewers that joined in the raid
---
