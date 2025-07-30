---
title: Permitted Terms Deleted
description: Trigger for when an a permitted term has been deleted
version: 0.2.4
variables:
  - name: createdAt
    type: datetime
    description: datetime of the deletion
    value: 28.06.2024 20:13:20
  - name: moderatorUsername
    type: string
    description: display name of the moderator who deleted the term
    value: Lyfesaver74
  - name: moderatorDisplayName
    type: string
    description: login name of the moderator who deleted the term
    value: lyfesaver74
  - name: moderatorId
    type: string
    description: display name of the moderator who deleted the term
    value: 161545467
  - name: termCount
    type: int
    description: amount of deleted terms
    value: 1
  - name: term.[#]
    type: string
    description: the number `#` of the term, starts with `0`, for example `term.[0], term[1]....term[n]`
    value: Peanutbutterhead
  - name: fromAutomod
    type: bool
    description: whether the term has been deleted from automod or not
    value: True/False
commonVariables:
  - TwitchBroadcaster
---
