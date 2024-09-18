---
title: Get Global Variable
description: Fetch the value of a global variable and populate a local argument
parameters:
  - name: GlobalVariableSource
  - name: GlobalVariablePersisted
  - name: Variable Name
    type: Text
    required: true
    description: |
      Enter the name of the variable you would like to fetch

      ::warning
      `Variable Name` must be entered in `camelCase` (the first letter must be lowercase)
      ::
  - name: Destination Variable
    type: Text
    required: true
    description: |
      Enter the name of the local argument you would like to populate

      ::tip
      It is recommended to use a **different name** than the global variable name
      ::
  - name: Default Value
    type: Text
    description: |
      Optionally set a default value

      This will create the global variable if it does not exist and then set it to the given value
variables:
  - name: <variableName>
    description: The variable name and type will be depend on the parameters you selected
csharpMethods:
  - GetGlobalVar
---

::tip
You can quickly access persisted globals without this sub-action by wrapping the name with `~`<br>
:icon{name=i-mdi-chevron-right} `~myGlobalVariable~`{lang=cs}
::

:read-more{to=/guide/variables}