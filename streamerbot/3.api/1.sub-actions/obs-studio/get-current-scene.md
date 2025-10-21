---
title: Get Current Scene
description: Get the current scene
parameters:
  - name: Connection
    import: obs-studio/connection
variables:
  - name: currentScene
    type: string
    description: Name of the active scene at the time of execution
    value: Gaming Scene
csharpMethods:
  - ObsGetCurrentScene
---