---
title: Load model
description: Load a selected model
parameters:
  - name: Model
    type: Selection
    required: true
    description: Select the model to be loaded
variables:
  - name: success
    type: bool
    description: Indicator whether the model has been loaded successfully or not
    value: True/False
csharpMethods:
  - VTubeStudioLoadModelById
  - VTubeStudioLoadModelByName
---
