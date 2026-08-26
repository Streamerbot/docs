---
title: Delete Points
description: Deletes all points from a specific user
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to delete points for
  - name: User
    type: Select
    required: true
    default: None
    description: The username of the user you want to delete points from (supports variables)
  - name: platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to delete points from (supports variables)
csharpMethods:
  - RemovePoints
---