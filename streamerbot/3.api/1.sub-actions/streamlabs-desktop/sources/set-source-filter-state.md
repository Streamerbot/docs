---
title: Set Source Filter State
description: Modify the visibility of a source filter
parameters:
  - name: SlobsConnection
  - name: SlobsScene
  - name: SlobsSource
  - name: State
    type: Select
    required: true
    description: |
      Select which state you want to set

      - `Visible`: Sets the filter state on your scene to Visible
      - `Hidden`: Sets the filter state on your scene to Hidden
      - `Toggle`: Toggles the filter state on your scene between Visible and Hidden
variables: []
csharpMethods:
  - SlobsSetFilterState
---
