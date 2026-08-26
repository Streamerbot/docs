---
title: Reset User Points
description: Reset the points of a specific user to 0
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
  - name: Destination Variable
    type: String
    required: false
    default: userPoints
    description: The argument variable name to store the users points after resetting to 0 (supports variables)
csharpMethods:
  - ResetUserPoints
---