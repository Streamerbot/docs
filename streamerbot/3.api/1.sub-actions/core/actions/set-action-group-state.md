---
title: Set Action Group State
description: Enable or disable a group of actions
parameters:
  - name: Group
    type: Select
    required: true
    default: None
    description: Choose the action group you want to enable or disable
  - name: State
    type: Select
    required: true
    description: |
      Choose the new state for all actions in the selected group.

      - `Enabled`: Enable all actions in the selected group
      - `Disabled`: Disable all actions in the selected group
      - `Toggle`: Toggle the current state of all actions in the selected group
    default: Enabled
---

::read-more{to="/api/sub-actions/core/actions/set-action-state"}
To modify the state of an individual action, see the [Set Action State](/api/sub-actions/core/actions/set-action-state) sub-action
::