---
title: Set Source Mute State
description: Mute or unmute a source in Streamlabs Desktop
parameters:
  - name: Connection
    import: streamlabs-desktop/connection
  - name: Scene
    import: streamlabs-desktop/scene
  - name: Source
    import: streamlabs-desktop/source
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
  - SlobsSetSourceMuteState
---
