---
title: Set Argument
description: Assign a custom variable for use by the following sub-actions
parameters:
  - name: Variable Name
    required: true
    type: Text
    description: |
      Enter the name of the variable you want to set.

      _Do not add the `%percent%`{lang=cs} symbols. Those only allow you to access your variable in later sub-actions_
  - name: Value
    required: true
    type: Text
    description: |
      Enter the new value to store with the given variable name

      ::tip
      You can use other [Variables](/guide/variables) or even manipulate existing arguments with [Inline Functions](/guide/variables#inline-functions)
      ::
  - name: Auto Type
    type: Toggle
    default: true
    description: |
      By default, all values are treated as text, or `string`{lang=cs} variables.

      Enable `Auto Type` to automatically determine the type for the entered value.

      For example:
      - `0`{lang=cs} can be auto-typed to a numeric type such as `int`{lang=cs} or `long`{lang=cs}
      - `true`{lang=cs} or `false`{lang=cs} can be auto-typed to a `bool`{lang=cs}
csharpMethods:
  - SetArgument
---

