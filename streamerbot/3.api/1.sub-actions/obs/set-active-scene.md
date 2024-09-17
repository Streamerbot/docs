---
title: Set Active Scene
description: Change the current scene
parameters:
  - name: ObsConnection
  - name: ObsScene
    type: Select
    required: true
    description: |
      Select a Scene from the drop-down
      - Can also manually type the Scene name into the box
variables: []
csharpMethods:
  - ObsSetScene
---