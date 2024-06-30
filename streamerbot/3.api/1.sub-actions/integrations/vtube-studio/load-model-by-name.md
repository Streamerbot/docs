---
title: Load Model By Name
description: Load a model by name
parameters:
  - name: Model
    type: String
    required: true
    description: Can be a specified model name or a variable. The name has to be exact, not case-sensitive though.
variables:
  - name: success
    type: bool
    description: Indicator whether the model has been loaded successfully or not
    value: True/False
csharpMethods:
  - VTubeStudioLoadModelById
  - VTubeStudioLoadModelByName
---
