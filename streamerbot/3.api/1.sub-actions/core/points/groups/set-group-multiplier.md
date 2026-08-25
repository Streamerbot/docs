---
title: Set Group Multiplier
description: Set the multiplier for a specific group
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to set the group multiplier for
  - name: Group
    type: Select
    required: true
    default: None
    description: Choose the group you want to set the multiplier for (supports variables)
  - name: Multiplier
    type: number
    required: true
    default: 1.0
    description: The multiplier for the selected group (supports variables)
csharpMethods:
  - SetGroupMultiplier
---