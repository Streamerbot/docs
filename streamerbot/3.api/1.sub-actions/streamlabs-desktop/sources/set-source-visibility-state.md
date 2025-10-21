---
title: Set Source Visibility State
description: Show or hide a source in Streamlabs Desktop
parameters:
  - name: Connection
    import: streamlabs-desktop/connection
  - name: Scene
    import: streamlabs-desktop/scene
  - name: Source
    import: streamlabs-desktop/source
  - name: State
    type: Select
    required: true
    description: Choose the desired visibility state for the selected source
    options:
      - value: Visible
        description: Set the visibility state to visible
      - value: Hidden
        description: Set the visibility state to hidden
      - value: Toggle
        description: Toggle the visibility state between visible and hidden
variables: []
csharpMethods:
  - SlobsSetSourceVisibility
---
