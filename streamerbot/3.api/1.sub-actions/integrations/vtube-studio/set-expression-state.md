---
title: Set Expression State
description: Set the expression state of the currently loaded model
parameters:
  - name: Expression
    type: Selection
    required: true
    description: Select an expression
  - name: State
    type: Selection
    required: true
    description: Choose between Toggle, Enabled or Disabled
variables:
  - name: success
    type: Bool
    description: indicator whether the expression state change has been successful or not
    value: True/False
csharpMethods:
  - VTubeStudioActivateExpression
  - VTubeStudioDeactivateExpression
---
