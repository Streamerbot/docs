---
title: Set Random Scene Source Visible
description: Select a random source from the selected scene and make it visible, if all items are visible, it will do nothing
parameters:
  - name: ObsConnection
  - name: ObsScene
    type: Select
    required: true
    description: |
      Select a Scene from the drop-down
      - Can also manually type the Scene name into the box
variables:
  - name: randomSource
    type: string
    description: name of the chosen random source
    value: Game Capture
csharpMethods:
  - ObsSetRandomSceneSourceVisible
---
