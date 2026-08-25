---
title: Award Points to All
description: Award points to all users
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to award points for
  - name: Amount
    type: number
    required: true
    default: 0
    description: The amount of points to award to all users (supports variables)
  - name: Platform
    type: string
    description: The platform to award points for (leave blank for all platforms)
  - name: Only Award to Active Users
    type: checkbox
    description: If checked, it will only award points to active users
  - name: Apply User/Group Multipliers
    type: checkbox
    description: If checked, it will apply any user/group multipliers to the awarded points
csharpMethods:
  - AwardPointsToAll
---