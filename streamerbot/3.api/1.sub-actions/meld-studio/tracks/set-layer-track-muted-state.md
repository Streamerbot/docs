---
title: Set Layer Track Muted State
description: Mute or unmute a Track associated with a Layer in Meld Studio
version: 0.2.5
parameters:
  - name: Connection
    import: meld-studio/connection
  - name: Scene
    import: meld-studio/scene
  - name: Layer
    import: meld-studio/layer
  - name: Track
    import: meld-studio/track
  - name: State
    type: Select
    required: true
    description: Select the mute state for the source
    options:
      - value: Muted
        description: Set the mute state to muted
      - value: Not Muted
        description: Set the mute state to not muted
      - value: Toggle
        description: Toggle the mute state between muted and not muted
variables: []
---
