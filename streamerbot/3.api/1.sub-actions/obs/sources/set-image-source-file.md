---
title: Set Image Source File
description: Set the file path for an image source (will accept image links as well)
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
  - name: Filename
    type: String
    required: true
    description: |
      The new filepath for the image source
variables: []
csharpMethods:
  - ObsSetImageSourceFile
---