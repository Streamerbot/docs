---
title: Set Global Variable
description: Create or update the value of a global variable
parameters:
  - name: Destination
    import: core/global-variable-destination
  - name: Persisted
    import: core/global-variable-persisted
  - name: Variable Name
    type: Text
    required: true
    description: |
      Enter the name of the global variable you would like to create or update

      ::warning
      `Variable Name` is the **name** of the global variable, which means it should not be wrapped in `%` symbols unless you specifically want to use the **value** of a local variable as the **name** of your global variable
      ::

  - name: Value
    type: Text
    required: true
    description: |
      Enter the value to assign to the global variable, depending on the selected type in the dropdown

      All options support parsing of %arguments%
      - `Value` - Enter any value
      - `Increment` - Enter any `int`{lang=cs} to be added to the existing value
      - `Decrement` - Enter any `int`{lang=cs} to be subtracted from the existing value

      ::tip
      If left empty, `Increment` and `Decrement` default to 1. If the global variable did not already exist, it will add or subtract from 0
      ::

variables: []
csharpMethods:
  - SetGlobalVar
---

::warning{to=/api/sub-actions/core/globals/global-get}
This **does not** also make the global variable's value available in your action<br/>
To access the value of a global variable in your action, you **must *first*** assign it to a local variable with the `Get Global Variable` sub-action
::

:read-more{to=/guide/variables}
