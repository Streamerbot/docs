---
title: Set Source Mute State
description: Mute or unmute a source
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
  - name: State
    type: Select
    required: true
    description: Select the mute status for the source
    options:
      - value: Muted
        description: Set the mute state to muted
      - value: Not Muted
        description: Set the mute state to not muted
      - value: Toggle
        description: Toggle the mute state between muted and not muted
variables: []
csharpMethods:
  - ObsSetSourceMuteState
---