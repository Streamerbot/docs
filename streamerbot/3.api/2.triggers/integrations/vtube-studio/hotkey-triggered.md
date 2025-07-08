---
title: Hotkey Triggered
description: Triggers every time a hotkey is triggered manually by the user (keyboard/hand-gesture) or via the hotkey-trigger-API
variables:
  - name: hotkeyId
    type: string
    description: The ID of the hotkey
    value: e47789a1545c4cae9753bf06d6dfe224
  - name: hotkeyName
    type: string
    description: The name of the hotkey
    value: Eyes Cry
  - name: hotkeyAction
    type: string
    description: The selected hotkey action
    value: ToggleExpression
  - name: hotkeyFile
    type: string
    description: The selected hotkey file
    value: EyesCry.exp3.json
  - name: hotkeyTriggeredByAPI
    type: bool
    description: flag whether a hotkey has been triggered by a plugin via the trigger-hotkey-API
    value: True/False
  - name: isLive2DItem
    type: bool
    description: Indicator whether it's a Live2D item or not
    value: True/False
commonVariables:
  - VTubeModel
---
