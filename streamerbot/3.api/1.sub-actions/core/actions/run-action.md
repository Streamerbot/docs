---
title: Run Action
description: Execute another Streamer.bot action
parameters:
  - name: Action
    type: Select
    required: true
    description: Choose the action you want to execute
  - name: Run Action Immediately
    type: Toggle
    default: true
    description: |
      When checked, the executed action will be run inline with the current set of sub-actions.

      Uncheck this if you want the action to run independently, in its own queue.
---

::tip
The executed action can populate its own variables which will then available to your calling action.
::