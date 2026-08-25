---
title: Remove Group Multiplier
description: Remove the multiplier for a specific group
version: 1.1.0
parameters:
  - name: Point Definition
    type: Select
    required: true
    default: None
    description: Choose the point definition you want to remove the group multiplier for
  - name: Group
    type: Select
    required: true
    default: None
    description: Choose the group you want to remove the multiplier for
csharpMethods:
  - RemoveGroupMultiplier
---