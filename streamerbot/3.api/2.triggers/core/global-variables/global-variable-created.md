---
title: Global Variable Created
description: Triggered when a global variable has been created
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
  - name: global.value
    type: string
    description: 
    value: My value
  - name: global.persisted
    type: bool
    description: 
    value: True
  - name: global.lastWrite
    type: DateTime
    description: 
    value: 8/4/2023 10:56:06 AM
---