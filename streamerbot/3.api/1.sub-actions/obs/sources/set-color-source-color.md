---
title: Set Color Source Color
description: Set a random or a HEX color for a color source
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
  - name: Random Color
    type: Checkbox
    required: false
    description: |
      This gets a random HEX color each time this sub-action runs
  - name: Color
    type: Color
    required: true
    description: |
      Choose a color, using the `#RRGGBBAA` format
variables: []
csharpMethods:
  - ObsSetColorSourceColor
  - ObsSetColorSourceRandomColor
---