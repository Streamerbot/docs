---
title: Set Sub-Action Weight
description: Changes the random weighting of specific sub-actions within an action
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
  - name: Weight
    type: Number
    required: true
    description: |
      Sets the new "weight" for the selected sub-action, which is the probability, relative to the other sub-actions' weights, that the sub-action will be chosen.

      For example, if all sub-action weights are the same, then they will all be equally likely to execute.

      If one sub-action's weight is double another's, then that sub-action will be chosen twice as often.
---

::tip
Only applies to sub-actions of an Action or sub-action group that is set to Random.
::
