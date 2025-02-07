---
title: Get Action Group State
description: Fetch the current enabled state of an action group
parameters:
  - name: Group
    type: Select
    required: true
    default: None
    description: Choose the action group you want to fetch the state of
variables:
  - name: actionGroupState
    type: number
    description: |
      State of the selected group
      - `0` - All actions in the group are disabled
      - `1` - All actions in the group are enabled
      - `2` - A mix of enabled and disabled actions
    value: 1
  - name: actionsEnabled
    type: List<string>
    description: List of all enabled action IDs from the selected group
  - name: actionsDisabled
    type: List<string>
    description: List of all disabled action IDs from the selected group
---
