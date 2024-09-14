---
title: Flip Source
description: Flip a source horizontally, vertically or both
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
  - name: Mode
    type: Select
    required: true
    description: |
      Select the direction to flip the source

      - `Horizontal`: Flip the source horizontally
      - `Vertical`: Flip the source vertically
      - `Both`: Flip the source horizontally and vertically
variables: []
csharpMethods: []
---