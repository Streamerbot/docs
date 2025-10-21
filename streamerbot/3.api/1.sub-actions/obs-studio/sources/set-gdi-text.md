---
title: Set GDI Text
description: Change the text value of GDI Text Source
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
  - name: Text
    type: String
    required: true
    description: |
      Enter the new text for the text source
variables: []
csharpMethods:
  - ObsSetGdiText
---