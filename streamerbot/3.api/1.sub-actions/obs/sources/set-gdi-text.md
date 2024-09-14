---
title: Set GDI Text
description: Change the text value of GDI Text Source
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
  - name: Text
    type: String
    required: true
    description: |
      Enter the new text for the text source
variables: []
csharpMethods:
  - ObsSetGdiText
---