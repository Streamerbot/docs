---
title: Get Command Group State
description: Get the current enabled state for all commands in a group
variables:
  - name: commandGroupState
    type: bool
    description: Current enabled state for the command group
    value: true
  - name: commandsEnabled
    type: Dictionary<Guid, Guid>
    description: List of all commands currently *enabled* within this command group
  - name: commandsDisabled
    type: Dictionary<Guid, Guid>
    description: List of all commands currently *disabled* within this command group
---

