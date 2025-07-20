---
title: Add Present User
description: Fetch info for a specified present user in your chat
parameters:
  - name: Index
    type: Int
    required: true
    description: can be a specific number or a variable like `%randomNumber%`. The index starts at `0`, so `0` will be the first user in your viewers list, `1` the second etc.
variables:
  - name: presentUsersCount
    type: int
    description: total number of present users
    value: 69
  - name: presentUser
    type: string/bool
    description: the user's display name, if the user was found // if no user was found, it will default to `False`
    value: GenericUser
  - name: presentUserName
    type: string
    description: the user's login name (unpopulated, if not user was found)
    value: genericuser
  - name: presentUserId
    type: string
    description: the user's ID (unpopulated, if not user was found)
    value: 12345678
  - name: presentUserType
    type: string
    description: the user's platform (unpopulated, if not user was found)
    value: twitch
csharpMethods: []
---
