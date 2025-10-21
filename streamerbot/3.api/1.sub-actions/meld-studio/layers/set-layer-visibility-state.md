---
title: Set Layer Visibility State
description: Show or hide a Layer
version: 0.2.5
parameters:
  - name: Connection
    import: meld-studio/connection
  - name: Scene
    import: meld-studio/scene
  - name: Layer
    import: meld-studio/layer
  - name: State
    type: Select
    required: true
    description: Select the state for the layer visibility
    options:
      - value: Visible
        description: Set the visibility state to visible
      - value: Hidden
        description: Set the visibility state to hidden
      - value: Toggle
        description: Toggle the visibility state between visible and hidden
variables: []
csharpmethods:
  - MeldStudioShowLayerByName
  - MeldStudioHideLayerByName
---
