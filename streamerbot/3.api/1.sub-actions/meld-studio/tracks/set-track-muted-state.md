---
title: Set Track Muted State
description: Mute or unmute a track
version: 0.2.5
parameters:
  - name: Connection
    import: meld-studio/connection
  - name: Layer
    import: meld-studio/layer
  - name: State
    type: Select
    required: true
    description: Select the mute state for the layer
    options:
      - value: Muted
        description: Set the mute state to muted
      - value: Not Muted
        description: Set the mute state to not muted
      - value: Toggle
        description: Toggle the mute state between muted and not muted
variables: []
---
