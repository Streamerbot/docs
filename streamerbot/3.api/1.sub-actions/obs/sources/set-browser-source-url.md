---
title: Set Browser Source Url
description: Change the URL of a browser source
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
  - name: Url
    type: String
    required: true
    description: |
      Enter a new URL for the browser source
variables: []
csharpMethods:
  - ObsSetBrowserSource
---