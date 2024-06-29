---
title: Set Channel Branded Content
description: Set the Branded Content state of your Twitch channel
version: 0.2.4
parameters:
  - name: State
    type: Select
    default: Enabled
    required: true
    description: |
      - `Enabled` - Enable the Branded Content state of your Twitch channel
      - `Disabled` - Disable the Branded Content state of your Twitch channel
      - `Toggle` - Toggle the existing state
variables:
  - name: success
    type: bool
    description: indictator whether the branded content has been set successfully
    value: True/False
---
