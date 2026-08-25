---
title: Check Points
description: Check the points of a specific user
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to check points for
  - name: User
    type: Select
    required: true
    default: None
    description: The username of the user you want to check points for (supports variables)
  - name: platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to check points for (supports variables)
  - name: Required Amount
    type: number
    required: true
    default: 0
    description: The minimum amount of points to check for (supports variables)
  - name: Break Action of Failure
    type: checkbox
    default: true
    description: If checked, it will break the action chain if the point check fails
  - name: Destination Variable
    type: String
    required: false
    default: userPoints
    description: The argument variable name to store the users points after awarding (supports variables)
csharpMethods:
  - GetPoints
---