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
    type: bool
    description: Enabled state of the selected action group
    value: true
  - name: actionsEnabled
    type: List<string>
    description: List of all enabled action IDs from the selected group
  - name: actionsDisabled
    type: List<string>
    description: List of all disabled action IDs from the selected group
---
