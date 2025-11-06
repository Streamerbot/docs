---
title: Get Global Variable
description: Fetch the value of a global variable and populate a local argument
parameters:
  - name: Source
    import: core/global-variable-source
  - name: Persisted
    import: core/global-variable-persisted
  - name: Variable Name
    type: Text
    required: true
    description: |
      Enter the name of the global variable you would like to fetch

      ::warning
      This is the **name** of the global variable, which means it should not be wrapped in `%` symbols unless you specifically want to use the **value** of a local variable in the **name** of your global variable
      ::

  - name: Destination Variable
    type: Text
    required: true
    description: |
      Enter the name of the local argument you would like to populate

      ::tip
      It is recommended to use a **different name** than the global variable name
      ::

      ::warning
      This is the **name** of the destination variable, which means it should not be wrapped in `%` symbols unless you specifically want to use the **value** of a local variable in the **name** of your destination variable
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
You can access the value of **persisted** non-user globals without this sub-action by wrapping the name with `~`<br>
:icon{name=i-mdi-chevron-right} For example, `~myPersistedGlobalVariable~`{lang=cs}
::

:read-more{to=/guide/variables}