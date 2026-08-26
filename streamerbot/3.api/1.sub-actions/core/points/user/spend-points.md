---
title: Spend Points
description: Spend points from a specific user
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to spend points for
  - name: User
    type: Select
    required: true
    default: None
    description: The username of the user you want to spend points from (supports variables)
  - name: platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to spend points from (supports variables)
  - name: Amount
    type: number
    required: true
    default: 0
    description: The amount of points to spend from the user (supports variables)
  - name: Break action sequence if user has insufficient points
    type: checkbox
    default: true
    description: If checked, the action sequence will be broken if the user has insufficient points
  - name: Destination Variable
    type: String
    required: false
    default: userPoints
    description: The argument variable name to store the users points after spending (supports variables)
csharpMethods:
  - SpendPoints
---