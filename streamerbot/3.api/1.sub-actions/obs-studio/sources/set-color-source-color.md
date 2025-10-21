---
title: Set Color Source Color
description: Set a random or a HEX color for a color source
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
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