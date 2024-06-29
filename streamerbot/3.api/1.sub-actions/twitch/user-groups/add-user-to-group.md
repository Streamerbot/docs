---
title: Add User To Group
description: Add a Twitch user to a group
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
  - name: addResult
    type: bool
    description: indicator whether the addition has been successful or not
    value: True/False
---

## C# Usage
:csharp-method{name=AddUserToGroup}
