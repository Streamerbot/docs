---
title: Trigger Hotkey
description: Trigger a hotkey in VTube Studio
parameters:
  - name: Model
    type: Selection
    required: true
    description: Select a model
  - name: Hotkey
    type: Selection
    required: true
    description: Select a hotkey action
variables:
  - name: success
    type: Bool
    description: indicator whether the hotkey trigger has been successful or not
    value: True/False
csharpMethods:
  - VTubeStudioTriggerHotkeyById
  - VTubeStudioTriggerHotkeyByName
---
