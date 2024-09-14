---
title: Set Source Mute State
description: Mute or unmute a source
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
  - name: State
    type: Select
    required: true
    description: |
      Select the mute status for the source

      - `Muted`: Set the mute state to muted
      - `Not Muted`: Set the mute state to not muted
      - `Toggle`: Toggle the mute state between muted and not muted
variables: []
csharpMethods:
  - ObsSetSourceMuteState
---