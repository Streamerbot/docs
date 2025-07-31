---
title: Blocked Terms Added
description: Trigger for when an a blocked term has been added
version: 0.2.4
variables:
  - name: createdAt
    type: datetime
    description: datetime of the addition
    value: 28.06.2024 20:13:20
  - name: moderatorUsername
    type: string
    description: display name of the moderator who added the term
    value: Lyfesaver74
  - name: moderatorDisplayName
    type: string
    description: login name of the moderator who added the term
    value: lyfesaver74
  - name: moderatorId
    type: string
    description: display name of the moderator who added the term
    value: 161545467
  - name: termCount
    type: int
    description: amount of added terms
    value: 1
  - name: term.[#]
    type: string
    description: the number `#` of the term, starts with `0`, for example `term.[0], term[1]....term[n]`
    value: Peanutbutterhead
  - name: fromAutomod
    type: bool
    description: whether the term has been added from automod or not
    value: True/False
commonVariables:
  - TwitchBroadcaster
---
