---
title: Set Random Scene Source Visible
description: Select a random source from the selected scene and make it visible
parameters:
  - name: ObsConnection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
variables:
  - description: name of the chosen random source
    name: randomSource
    type: string
    value: Game Capture
csharpMethods:
  - ObsSetRandomSceneSourceVisible
---

::warning
If all items within the scene are already visible, this sub-action will do nothing.
::