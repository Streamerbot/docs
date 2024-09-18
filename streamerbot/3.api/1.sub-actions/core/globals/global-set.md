---
title: Set Global Variable
description: Create or update a global variable
parameters:
  - name: GlobalVariableSource
  - name: GlobalVariablePersisted
  - name: Variable Name
    type: Text
    required: true
    description: |
      Enter the name of the variable you would like to create or modify

      ::warning
      `Variable Name` must be entered in `camelCase` (the first letter must be lowercase)
      ::
  - name: Source
    type: Select
    default: Argument
    required: true
    description: |
      Select the source for the value to assign to the global variable

      - `Argument` - Use the value of an argument
      - `Value` - Assign any arbitrary value
      - `Increment` - Add to an existing `int`{lang=cs} variable
      - `Decrement` - Subtract from an existing `int`{lang=cs} variable
  - name: Value
    type: Text
    required: true
    description: |
      Enter the value to assign to the global variable, depends on the selected `Source` type, detailed above

      - `Argument` - Enter the name of an existing argument to assign its value to the global variable
      - `Value` - Enter any value
      - `Increment` - Enter any `int`{lang=cs}
      - `Decrement` - Enter any `int`{lang=cs}
variables: []
csharpMethods:
  - SetGlobalVar
---

:read-more{to=/guide/variables}
