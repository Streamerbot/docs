---
title: Set Image Source File
description: Set the file path for an image source (will accept image links as well)
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
  - name: Filename
    type: String
    required: true
    description: |
      The new filepath for the image source
variables: []
csharpMethods:
  - ObsSetImageSourceFile
---