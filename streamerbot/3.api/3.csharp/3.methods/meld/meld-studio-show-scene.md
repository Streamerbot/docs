---
name: MeldStudioShowScene
title: MeldStudioShowScene
description: Shows the selected Meld Studio Scene by ID
parameters:
  - name: sceneId
    type: text
    description: Enter the Scene Id
  - name: connectionIdx
    type: number
    default: -1
    description: Enter the connection index number (`-1` is a fallback for the `Default` connection)
version: 0.2.5
---