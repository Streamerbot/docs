---
title: Set Trigger State
description: Sets the Trigger State for an individual trigger on a specified action
version: 0.2.5
parameters:
  - name: Action
    type: Select
    description: Select the desired Action to modify
  - name: Triggers
    type: Select
    description: Select the Trigger from the selected Action
  - name: State
    type: Select
    description: |
      Select the new state for the Trigger

      - `Enabled`: Enable the selected Trigger
      - `Disabled`: Disable the selected Trigger
      - `Toggle`: Toggle the existing state of the selected Trigger
---
