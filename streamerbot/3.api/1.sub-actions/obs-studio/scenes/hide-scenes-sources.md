---
title: Hide Scene's Sources
description: Hide ALL sources within the given Scene
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
  - ObsHideSceneSources
---