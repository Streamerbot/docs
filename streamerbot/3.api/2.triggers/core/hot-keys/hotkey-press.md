---
title: HotKey Press
description: Trigger for a HotKey Press
variables:
  - name: modifier
    type: number
    description: The amount of modifiers
    value: 2
  - name: hasCtrl
    type: boolean
    description: If the hotkey press uses <kbd>CTRL</kbd>
    value: True
  - name: hasAlt
    type: boolean
    description: If the hotkey press uses <kbd>ALT</kbd>
    value: True
  - name: hasShift
    type: boolean
    description: If the hotkey press uses <kbd>SHIFT</kbd>
    value: True
  - name: key
    type: number
    description: The numeric key value
    value: 48
---

:image-preview

## Parameters
::field-group
  ::field{name=HotKey type=Select}
    Select a HotKey from the Hot Keys tab

    - Select `Any` to trigger on **any hotkey**

    ::tip{color=amber}
    You can quickly register a new HotKey by clicking the `Create HotKey` button!
    ::
  ::
::