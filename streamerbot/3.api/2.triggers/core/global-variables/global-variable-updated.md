---
title: Global Variable Updated
description: Triggered when a global variable has been updated
version: 0.2.1
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
    version: 0.2.3
    description: |
      - `Either` - Trigger on **both** persisted and non-persisted variables
      - `Yes` - Trigger only on **persisted** variables
      - `No` - Trigger only on **non-persisted** variables
variables:
  - name: global.name
    type: string
    description: The name of the global variable
    value: myGlobalVariable
  - name: global.newValue
    type: string
    description: The new value of the global variable
    value: My new value
  - name: global.oldValue
    type: string
    description: The previous value of the global variable
    value: My old value
  - name: global.persisted
    type: bool
    description: Is this global variable persisted?
    value: True
  - name: global.lastWrite
    type: DateTime
    description: The timestamp of the last write
    value: 8/4/2023 10:56:06 AM
---