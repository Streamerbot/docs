---
title: Get User Multiplier
description: Retrieve the multiplier for a specific user
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to retrieve the multiplier for
  - name: User
    type: Select
    required: true
    default: None
    description: The username of the user you want to retrieve the multiplier for (supports variables)
  - name: platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to retrieve the multiplier for (supports variables)
  - name: Destination Variable
    type: String
    required: false
    default: userMultiplier
    description: The argument variable name to store the effective multiplier value (supports variables)
csharpMethods:
  - GetUserMultiplier
---