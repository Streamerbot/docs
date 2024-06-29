---
title: Set Background Color
description: Set the background color for a Twitch channel point reward
parameters:
  - name: Reward
    type: Select
    required: true
    description: Select the channel point reward
  - name: Random Color
    type: Checkbox
    required: false
    description: Check to select a random color
  - name: Color
    type: String
    required: true
    description: hex color code
---

::tip
The reward must have been created in StreamerBot (owned) in order to edit it.
::

## C# Usage
:csharp-method{name=UpdateRewardBackgroundColor}
