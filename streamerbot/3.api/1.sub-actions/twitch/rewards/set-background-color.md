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
csharpMethods:
  - UpdateRewardBackgroundColor
---

::tip
The reward must have been created through Streamer.bot (owned by your bot) in order to edit it.
::
