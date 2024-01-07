---
title: Global Variable Updated
description: Trigger for when a Global Variable is Updated
version: 0.2.1
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
    description: The old value of the global variable
    value: My old value
  - name: global.persisted
    type: boolean
    description: Is this global variable persisted?
    value: True
  - name: global.lastWrite
    type: DateTime
    description: The timestamp of the last write
    value: 8/4/2023 10:56:06 AM
---

:image-preview

## Parameters
::field-group
  ::field{name="Variable Name" type=Text}
    Input the name of the global variable

    - Leaving the variable name empty is considered a catch-all and this will trigger on **any** global variable
  ::
::