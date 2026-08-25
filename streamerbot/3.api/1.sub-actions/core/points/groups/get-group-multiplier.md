---
title: Get Group Multiplier
description: Fetch the multiplier for a specific group
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to fetch the group multiplier for
  - name: Group
    type: Select
    required: true
    default: None
    description: Choose the group you want to fetch the multiplier for (supports variables)
  - name: Destination Variable
    type: string
    description: The variable to store the fetched group multiplier
csharpMethods:
  - GetGroupMultiplier
---