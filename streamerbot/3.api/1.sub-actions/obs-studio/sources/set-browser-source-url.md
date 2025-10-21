---
title: Set Browser Source Url
description: Change the URL of a browser source
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
  - name: Url
    type: String
    required: true
    description: |
      Enter a new URL for the browser source
variables: []
csharpMethods:
  - ObsSetBrowserSource
---