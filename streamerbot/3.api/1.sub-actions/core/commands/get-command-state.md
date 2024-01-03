---
title: Get Command State
description: Check the current enabled state of a command
variables:
  - name: commandState
    type: bool
    description: The current enabled state of this command
    value: true
---

You could use this to check if a command is enabled or disabled. This value is stored in the Boolean variable `commandState` and can be `True` or `False`.

![get_command_state_dialog_box.png](/get-command-state/get_command_state_dialog_box.png =400x)

## Parameters
::field-group
  ::field{name=Command type=Dropdown}
  Select an existing command to get its state
  ::
::