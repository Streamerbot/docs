---
title: Get Command Group State
description: Get the current enabled state for all commands in a group
variables:
  - name: commandGroupState
    type: number
    description: Current enabled state for the command group
    value: '0 = Enabled | 1 = Disabled | 2 = Mixed'
  - name: commandsEnabled
    type: Dictionary<Guid, Guid>
    description: List of all commands currently *enabled* within this command group
  - name: commandsDisabled
    type: Dictionary<Guid, Guid>
    description: List of all commands currently *disabled* within this command group
---

