---
title: Get Points
description: Retrieve the points of a specific user
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to retrieve points for
  - name: User
    type: Select
    required: true
    default: None
    description: The username of the user you want to retrieve points for (supports variables)
  - name: platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to retrieve points for (supports variables)
  - name: Destination Variable
    type: String
    required: false
    default: userPoints
    description: The argument variable name to store the users points (supports variables)
csharpMethods:
  - GetPoints
---