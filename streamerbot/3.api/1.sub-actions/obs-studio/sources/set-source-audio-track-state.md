---
title: Set Source Audio Track State
description: Set the audio track state on a source
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
  - name: Track
    type: Select
    required: true
    description: Select which audio track to change to
    options:
      - value: Track 1
        description: Set source audio to Track 1
      - value: Track 2
        description: Set source audio to Track 2
      - value: Track 3
        description: Set source audio to Track 3
      - value: Track 4
        description: Set source audio to Track 4
      - value: Track 5
        description: Set source audio to Track 5
      - value: Track 6
        description: Set source audio to Track 6
  - name: State
    type: Select
    required: true
    description: Select an audio track state
    options:
      - value: Active
        description: Sets the audio track state to Active
      - value: Inactive
        description: Sets the audio track state to Inactive
      - value: Toggle
        description: Toggles the audio track state between Active and Inactive
variables: []
csharpMethods: []
---