---
title: Remove User From Group
description: Remove a Twitch user from a group
parameters:
  - name: User Login
    type: String
    required: true
    description: can be a user name or a variable like `%userName%`
  - name: Group Name
    type: String
    required: true
    description: can be a specific group name or a variable
variables:
  - name: removeResult
    type: bool
    description: indicator whether the removal has been successful or not
    value: True/False
---

## C# Usage
:csharp-method{name=RemoveUserFromGroup}
