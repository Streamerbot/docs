---
title: Users Added
description: Triggers when a user gets added to a group.
version: 0.2.5
variables:
  - name: group.id
    type: Guid
    description: The ID of the group
    value: 48cdafcf-92e7-420e-ad99-70038b2bc0d4
  - name: group.name
    type: string
    description: The name of the group
    value: Members
  - name: group.bots
    type: bool
    description: Indicator whether the group is a Bots group
    value: False
  - name: group.user.count
    type: int
    description: The amount of users added to the group
    value: 1
  - name: group.user#.userId
    type: string
    description: The ID of the added user (indexed, starting with `0`, e.g. `group.user0.userId`)
    value: 29338059
  - name: group.user#.user
    type: string
    description: The display name of the added user (indexed, starting with `0`, e.g. `group.user0.user`)
    value: Lyfesaver74
  - name: group.user#.userName
    type: string
    description: The login name of the added user (indexed, starting with `0`, e.g. `group.user0.userName`)
    value: Lyfesaver74
  - name: group.user#.userType
    type: string
    description: The platform type of the added user (indexed, starting with `0`, e.g. `group.user0.userType`)
    value: twitch
  - name: group.user#.isSubscribed
    type: bool
    description: Indicator whether the added user is subscribed (indexed, starting with `0`, e.g. `group.user0.isSubscribed`)
    value: True
commonVariables: []
---
