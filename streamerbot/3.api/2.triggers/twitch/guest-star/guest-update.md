---
title: Guest Star Guest Update
description: Trigger for when a Guest Star guest receives an update
version: 0.2.3
parameters:
  - name: Scene Name
    type: Select
    version: 0.2.5
    required: false
    description: |
      Defaults to 'Any', but can select 'Selected', 'Backstage', 'Invited', 'Live', 'Ready', or 'Removed'
variables:
  - name: sessionId
    type: string
    description: ID of the current session
    value: 2iWsVXrc5WBsHr8ILWXYa9mAmOo
  - name: moderatorUserName
    type: string
    description: display name of the moderator who updated the guest settings
    value: Lyfesaver74
  - name: moderatorUserLogin
    type: string
    description: login name of the moderator who updated the guest settings
    value: lyfesaver74
  - name: moderatorUserId
    type: string
    description: user ID of the moderator who updated the guest settings
    value: 161545467
  - name: guestUserName
    type: string
    description: display name of the guest
    value: Lyfesaver74
  - name: guestUserLogin
    type: string
    description: login name of the guest
    value: lyfesaver74
  - name: guestUserId
    type: string
    description: user ID of the guest
    value: 161545467
  - name: slotId
    type: string
    description: ID of the guest slot
    value: 123 (<null> if not joined)
  - name: state
    type: string
    description: guest update state
    value: invited, backstage, ready
  - name: hostVideoEnabled
    type: bool
    description: video enabled status
    value: True/False (<null> if not joined)
  - name: hostAudioEnabled
    type: bool
    description: audio enabled status
    value: True/False (<null> if not joined)
  - name: hostVolume
    type: number
    description: video enabled status
    value: 100 (<null> if not joined)
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---
