---
title: Transfer Points
description: Transfer points from one user to another
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to transfer points for
  - name: Source User
    type: Select
    required: true
    default: None
    description: The username of the user you want to transfer points from (supports variables)
  - name: Source Platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to transfer points from (supports variables)
  - name: Target User
    type: Select
    required: true
    default: None
    description: The username of the user you want to transfer points to (supports variables)
  - name: Target Platform
    type: String
    required: true
    default: '%userType%'
    description: The platform of the user you want to transfer points to (supports variables)
  - name: Amount
    type: number
    required: true
    default: 0
    description: The amount of points to transfer (supports variables)
  - name: Base Variable Name
    type: String
    required: false
    default: userPoints
    description: Outputs '%(variableName)Source%' and '%(variableName)Target%' with the users points after the transfer (supports variables)
csharpMethods:
  - TransferPoints
---