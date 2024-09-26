---
title: Set Source Visibility State
description: Show or hide a source in Streamlabs Desktop
parameters:
  - name: SlobsConnection
  - name: SlobsScene
  - name: SlobsSource
  - name: State
    type: Select
    required: true
    description: |
      Choose the desired visibility state for the selected source

      - `Visible`: Set the visibility state to visible
      - `Hidden`: Set the visibility state to hidden
      - `Toggle`: Toggle the visibility state between visible and hidden
variables: []
csharpMethods:
  - SlobsSetSourceVisibility
---
