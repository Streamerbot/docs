---
title: Set Sub-Action Weight
description: Changes the random weighting of specific sub-actions within an action
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
    type: float
    required: true
    description: |
      Sets the new "weight" for the selected sub-action, which is the probability, relative to the other subactions' weights, that the subaction will be chosen. For example, if all subaction weights are the same, then they will all be equally likely. If one subaction's weight is double another's, then that subaction will be chosen twice as often.
---
::tip
Only applies to subactions of an Action or sub-action group that is set to Random.
::
