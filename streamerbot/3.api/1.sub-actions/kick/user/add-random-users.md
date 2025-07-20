---
title: Add Random Users
description: Get a custom amount of random Kick users
parameters:
  - name: Count
    type: Int
    required: true
    description: Specify the amount of random users with number or a variable like `%randomNumber%`.
  - name: Present Only
    type: Toggle
    default: false
    description: If checked will only get random users from the current present viewers. If count is bigger than the current amount of viewers it will only populate max the amount of viewers.
  - name: Include Groups
    type: Toggle
    default: false
    description: If checked will include groups in the random users. Select a group from the dropdown and press 'Add' to add it to the list. 
variables:
  - name: randomUser#
    type: string
    description: The random user's display name, with `#` index starting at 0
    value: StreamerDotBot
  - name: randomUserName#
    type: string
    description: The random user's login name, with `#` index starting at 0
    value: streamerdotbot
  - name: randomUserId#
    type: string
    description: The random user's id, with `#` index starting at 0
    value: 12345678
  - name: randomUserType#
    type: string
    description: the random user's platform, with `#` index starting at 0
    value: kick
csharpMethods: []
---