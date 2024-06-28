---
title: Blocked Termes Added
description: Trigger for when an AutoMod message is held
version: 0.2.4
variables:
  - name: createdAt
    type: datetime
    description: datetime of the unban
    value: 28.06.2024 20:13:20
  - name: moderator.userName
    type: string
    description: display name of the moderator who did the warning
    value: Lyfesaver74
  - name: moderator.login
    type: string
    description: login name of the moderator who did the warning
    value: lyfesaver74
  - name: moderator.id
    type: string
    description: display name of the moderator who did the warning
    value: 161545467
  - name: reason
    type: string
    description: the reason specified in the warning
    value: spam
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
  - TwitchUser
---
