---
title: Set Scene Filter State
description: Sets the visibility state of a scene filter
parameters:
  - name: ObsConnection
  - name: ObsScene
    type: Select
    required: true
    description: |
      Select a Scene from the drop-down
      - Can also manually type the Scene name into the box
  - name: ObsFilter
    type: Select
    required: true
    description: |
      Select a Filter from the drop-down
      - Can also manually type the Filter name into the box
  - name: State
    type: Select
    required: true
    description: |
      Select the state for the filter

      - `Visible`: Set the filter state to visible
      - `Hidden`: Set the filter state to hidden
      - `Toggle`: Toggle the filter state between visible and hidden
variables: []
csharpMethods:
  - ObsSetSceneFilterState
---