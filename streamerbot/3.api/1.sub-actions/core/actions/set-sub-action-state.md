---
title: Set Sub-Action State
description: Enable or disable specific sub-actions within an action
version: 1.0.0
parameters:
  - name: Action
    type: Select
    required: true
    description: Choose the parent action of the sub-action you wish to modify
  - name: Sub-Action
    type: Select
    required: true
    description: Choose the specific sub-action you wish to modify
  - name: State
    type: Select
    required: true
    description: |
      Choose the new state for the selected sub-action

      - `Enabled`: Enable the selected sub-action
      - `Disabled`: Disable the selected sub-action
      - `Toggle`: Toggle the current state of the selected sub-action
    default: Enabled
---

::read-more{to="/api/sub-actions/core/actions/set-action-state"}
To modify the state of an entire action, and all sub-actions, see the [Set Action State](/api/sub-actions/core/actions/set-action-state) sub-action
::
