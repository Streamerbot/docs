---
title: Award Points
description: Award points to a specific user
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to award points for
  - name: User
    type: Select
    required: true
    default: None
    description: The username of the user you want to award points to (supports variables)
  - name: platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to award points to (supports variables)
  - name: Amount
    type: number
    required: true
    default: 0
    description: The amount of points to award to all users (supports variables)
  - name: Apply User/Group Multipliers
    type: checkbox
    description: If checked, it will apply any user/group multipliers to the awarded points
  - name: Destination Variable
    type: String
    required: false
    default: userPoints
    description: The argument variable name to store the users points after awarding (supports variables)
csharpMethods:
  - AddPoints
---