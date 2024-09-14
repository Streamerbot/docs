---
title: Get Current Scene
description: Get the current scene
parameters:
  - name: ObsConnection
    type: Select
    required: true
    description: |
      Select the Connection from the drop-down
      - Any, Default, or named connections will appear here
variables:
  - name: currentScene
    type: string
    description: Name of the active scene at the time of execution
    value: Gaming Scene
csharpMethods:
  - ObsGetCurrentScene
---