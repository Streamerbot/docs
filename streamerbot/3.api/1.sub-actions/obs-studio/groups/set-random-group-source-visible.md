---
title: Set Random Group Source Visible
description: Set a random source from a group visible
parameters:
  - name: ObsConnection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Group
    import: obs-studio/group
variables:
  - description: name of the chosen random source
    name: randomSource
    type: string
    value: Game Capture
csharpMethods:
  - ObsSetRandomGroupSourceVisible
---
