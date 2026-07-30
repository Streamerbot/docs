---
title: Delay
description: Add a delay between sub-actions
parameters:
  - name: Delay
    type: Number
    required: true
    description: The duration of the delay
  - name: Random
    type: Checkbox
    description: Generate a random delay between min/max values
  - name: To
    type: Checkbox
    description: If `Random` is selected, a random delay will be selected between the `Delay` and `To` values
variables: []
csharpMethods:
  - Wait
---
