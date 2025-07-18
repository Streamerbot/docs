---
title: Global Variable Deleted
description: Triggered when a global variable has been deleted
version: 
parameters:
  - name: Variable Name
    type: Text
    description: |
      Enter the name of a specific global variable

      Leave empty to trigger on **any** global variable.
  - name: Persisted
    type: Select
    required: true
    default: Either
    version: 
    description: |
      - `Either` - Trigger on **both** persisted and non-persisted variables
      - `Yes` - Trigger only on **persisted** variables
      - `No` - Trigger only on **non-persisted** variables
variables:
  - name: global.name
    type: string
    description: 
    value: myGlobalVariable
  - name: global.persisted
    type: bool
    description: 
    value: True
---