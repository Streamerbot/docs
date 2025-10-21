---
title: Get Current Scene
description: Get the current scene from Streamlabs Desktop
parameters:
  - name: Connection
    import: streamlabs-desktop/connection
variables:
  - name: currentScene
    description: Name of the active scene
    type: string
    value: My Scene
csharpMethods:
  - SlobsGetCurrentScene
---