---
title: Set Random Group Source Visible
description: Set a random source from a group visible
parameters:
  - name: ObsConnection
  - name: ObsScene
    type: Select
    required: true
    description: |
      Select a Scene from the drop-down
      - Can also manually type the Scene name into the box
  - name: ObsGroup
    type: Select
    required: true
    description: |
      Select a Group from the drop-down
      - Can also manually type the Group name into the box
variables: []
csharpMethods:
  - ObsSetRandomGroupSourceVisible
---