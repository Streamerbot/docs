---
title: Add User To Group
description: Add a Kick user to a group
parameters:
  - name: User Login
    type: String
    required: true
    description: can be a user name or a variable like `%userName%`
    value: Amouranth
  - name: Group Name
    type: String
    required: true
    description: can be a specific group name or a variable
    value: BestFriends
variables:
  - name: addResult
    type: bool
    description: indicator whether the addition has been successful or not
    value: True/False
---
