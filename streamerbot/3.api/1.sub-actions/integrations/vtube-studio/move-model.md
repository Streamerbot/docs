---
title: Move Model
description: Mode the currently loaded model
parameters:
  - name: Time in Seconds
    type: Float
    required: true
    description: Time in seconds the movement should take (has to be between 0 and 2)
  - name: Relative to Model
    type: Bool
    required: true
    description: Flag whether the values are relative to the model's current position
  - name: Position X
    type: Float
    required: false
    description: X Position of the model (between -1 and 1, see image)
  - name: Position Y
    type: Float
    required: false
    description: Y Position of the model (between -1 and 1, see image)
  - name: Rotation
    type: Float
    required: false
    description: Rotation of the model (between -360 and 360, see image)
  - name: Size
    type: Float
    required: false
    description: Size of the model (between -100 and 100)
variables:
  - name: success
    type: bool
    description: indicator whether the movement has been successful or not
    value: True/False
csharpMethods:
  - VTubeStudioMoveModel
---

## The VTS Coordinate System
![VTS Coordinate System](assets/vts-coordinate-system.png)
