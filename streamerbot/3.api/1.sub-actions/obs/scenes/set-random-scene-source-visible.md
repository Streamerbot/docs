---
title: Set Random Scene Source Visible
description: Select a random source from the selected scene and make it visible, if all items are visible, it will do nothing
parameters:
  - name: ObsConnection
    type: Select
    required: true
    description: |
      Select the Connection from the drop-down
      - Any, Default, or named connections will appear here
  - name: ObsScene
    type: Select
    required: true
    description: |
      Select a Scene from the drop-down
      - Can also manually type the Scene name into the box   
variables: []
csharpMethods:
  - ObsSetRandomSceneSourceVisible
---