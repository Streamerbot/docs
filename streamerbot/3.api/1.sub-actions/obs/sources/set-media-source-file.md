---
title: Set Media Source File
description: Set the file path for a media source
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
      The new filepath for the media source
variables: []
csharpMethods:
  - ObsSetMediaSourceFile
---