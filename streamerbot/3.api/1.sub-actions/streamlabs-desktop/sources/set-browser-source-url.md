---
title: Set Browser Source URL
description: Modify the URL of a browser source
parameters:
  - name: Connection
    import: streamlabs-desktop/connection
  - name: Scene
    import: streamlabs-desktop/scene
  - name: Source
    import: streamlabs-desktop/source
  - name: URL
    type: Text
    required: true
    description: Enter the new URL for the selected browser source
variables: []
csharpMethods:
  - SlobsSetBrowserSource
---