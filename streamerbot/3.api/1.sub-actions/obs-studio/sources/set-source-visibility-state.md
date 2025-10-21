---
title: Set Source Visibility State
description: Show or hide a source
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Scene
    import: obs-studio/scene
  - name: Source
    import: obs-studio/source
  - name: State
    type: Select
    required: true
    description: Select the state for the source visibility state
    options:
      - value: Visible
        description: Set the source visibility to visible
      - value: Hidden
        description: Set the source visibility to hidden
      - value: Toggle
        description: Toggle the source visibility between visible and hidden
variables: []
csharpMethods:
  - ObsSetSourceVisibility
---