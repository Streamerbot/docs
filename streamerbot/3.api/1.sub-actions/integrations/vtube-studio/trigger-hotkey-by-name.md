---
title: Trigger Hotkey by Name
description: Trigger a hotkey in VTube Studio by name
parameters:
  - name: Name
    type: String
    required: true
    description: Can be a specific name or a variable
variables:
  - name: success
    type: Bool
    description: indicator whether the hotkey trigger has been successful or not
    value: True/False
csharpMethods:
  - VTubeStudioTriggerHotkeyById
  - VTubeStudioTriggerHotkeyByName
---
