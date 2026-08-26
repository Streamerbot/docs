---
title: Update Points
description: Update the point balance for a specific user
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to update points for
  - name: User
    type: Select
    required: true
    default: None
    description: The username of the user you want to update points for (supports variables)
  - name: platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to update points for (supports variables)
  - name: Amount
    type: number
    required: true
    default: 0
    description: The amount of points to update (supports variables)
  - name: Apply User/Group Multipliers
    type: checkbox
    description: If checked, it will apply any user/group multipliers to the updated points
  - name: Destination Variable
    type: String
    required: false
    default: userPoints
    description: The argument variable name to store the users points after updating (supports variables)
csharpMethods:
  - UpdatePoints
  - UpdateBulkPoints
---