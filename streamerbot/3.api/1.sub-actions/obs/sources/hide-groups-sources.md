---
title: Hide Group's Sources
description: Hide all the sources from a group
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
  - name: ObsGroup
    type: Select
    required: true
    description: |
      Select a Group from the drop-down
      - Can also manually type the Group name into the box
variables: []
csharpMethods:
  - ObsHideGroupsSources
---