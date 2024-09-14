---
title: Set Source Audio Track State
description: Set the audio track state on a source
parameters:
  - name: ObsConnection
    type: Select
    required: true
    description: |
      Select the Connection from the drop-down
      - Any, Default, or named connections will appear here
  - name: ObsScene
    type: Select
    required: true
    description: |
      Select a Scene from the drop-down
      - Can also manually type the Scene name into the box
  - name: ObsSource
    type: Select
    required: true
    description: |
      Select a Source from the drop-down
      - Can also manually type the Source name into the box
  - name: Track
    type: Select
    required: true
    description: |
      Select which audio track to change to
      - Options: `Track 1`, `Track 2`, `Track 3`, `Track 3`, `Track 5`, `Track 6`
  - name: State
    type: Select
    required: true
    description: |
      Select an audio track state

      - `Active`: Sets the audio track state to Active
      - `Inactive`: Sets the audio track state to Inactive
      - `Toggle`: Toggles the audio track state between Active and Inactive
variables: []
csharpMethods: []
---