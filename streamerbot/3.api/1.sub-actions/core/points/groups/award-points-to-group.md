---
title: Award Points to Group
description: Award points to all users in the specified group
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to award points for
  - name: Group
    type: Select
    required: true
    default: None
    description: Choose the group you want to award points to (supports variables)
  - name: Amount
    type: number
    required: true
    default: 0
    description: The amount of points to award to all users (supports variables)
  - name: Apply User/Group Multipliers
    type: checkbox
    description: If checked, it will apply any user/group multipliers to the awarded points
csharpMethods:
  - AwardPointsToGroup
---