---
title: Model Clicked
description: Triggers every time the model is clicked. Depending on the config, it also triggers when you click anywhere in the VTS window even if the click wasn't on the model.
version: 0.2.4
variables:
  - name: modelLoaded
    type: bool
    description: Flag whether the model has been loaded or not.
    value: True/False
  - name: modelId
    type: string
    description: The model's ID
    value: 62c6a71a4d324204afd25f61445f8e4f
  - name: modelName
    type: string
    description: The model's name
    value: Hijiki
  - name: modelWasClicked
    type: bool
    description: Flag whether the model has been clicked or not.
    value: True/False
  - name: mouseButtonId
    type: int
    description: The ID of the mouse button (0 is left-click, 1 is right-click and 2 is middle-click (mouse-wheel click))
    value: 0
  - name: clickPosition.X
    type: double
    description: The X position of the click in the usual coordinate system
    value: 0.276041656732559
  - name: clickPosition.Y
    type: double
    description: The Y position of the click in the usual coordinate system
    value: 0.0166666675359011
  - name: windowSize.X
    type: int
    description: current VTS X axis window size in pixels
    value: 1920
  - name: windowSize.Y
    type: int
    description: current VTS Y axis window size in pixels
    value: 1080
  - name: clickedArtMeshCount
    type: int
    description: The number of ArtMeshes at the click position if the model was clicked
    value: 0
---
