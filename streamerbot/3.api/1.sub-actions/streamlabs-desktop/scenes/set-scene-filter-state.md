---
title: Set Scene Filter State
description: Update the visibility of a filter for a given scene
parameters:
  - name: SlobsConnection
  - name: SlobsScene
  - name: SlobsFilter
  - name: State
    type: Select
    required: true
    description: |
      Select the new state for the selected filter

      - `Visible`: Sets the filter state on your scene to Visible
      - `Hidden`: Sets the filter state on your scene to Hidden
      - `Toggle`: Toggles the filter state on your scene between Visible and Hidden
variables: []
csharpMethods:
  - SlobsSetFilterState
---
