---
title: Set State of a Random Filter
description: Set the state of a filter randomly selected from a given scene or source
parameters:
  - name: SlobsConnection
  - name: SlobsScene
  - name: SlobsSource
  - name: State
    type: Select
    required: true
    description: |
      Set the state for the random filter

      - `Visible`: Set the filter state to visible
      - `Hidden`: Set the filter state to hidden
      - `Toggle`: Toggle the filter state between visible and hidden
variables: []
csharpMethods:
  - SlobsSetRandomFilterState
---
