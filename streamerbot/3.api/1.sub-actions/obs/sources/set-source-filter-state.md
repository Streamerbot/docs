---
title: Set Source Filter State
description: Sets the visibility state of a source filter
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
  - name: ObsSource
    type: Select
    required: true
    description: |
      Select a Source from the drop-down
      - Can also manually type the Source name into the box
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
  - ObsSetSourceFilterState
---