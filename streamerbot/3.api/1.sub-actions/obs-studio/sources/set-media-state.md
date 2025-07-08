---
title: Set Media State
description: Set the status of the media source
parameters:
  - name: ObsConnection
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
      Select the playback state for the selected Media

      - `Play`: Play your Media Source
      - `Pause`: Pause your Media Source
      - `Restart`: Restart your Media Source
      - `Stop`: Stop your Media Source
      - `Next`: Go next on your Media Source
      - `Previous`: Go to the previous on your Media Source
variables: []
csharpMethods:
  - ObsSetMediaState
---