---
title: Set Action State
description: Enable or disable a specific action
parameters:
  - name: Action
    type: Select
    required: true
    description: Choose the action you want to enable or disable
  - name: State
    type: Select
    required: true
    description: |
      Choose the new state for the selected action

      - `Enabled`: Enable the selected action
      - `Disabled`: Disable the selected action
      - `Toggle`: Toggle the current state of the selected action
    default: Enabled
---

::read-more{to="/api/sub-actions/core/actions/set-action-group-state"}
To modify the state of an entire action group, see the [Set Action Group State](/api/sub-actions/core/actions/set-action-group-state) sub-action
::