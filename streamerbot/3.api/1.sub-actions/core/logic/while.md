---
title: While
description: Allow for looping of sub-actions
version: 1.0.0
parameters:
  - name: Input
    type: Text
    required: true
    description: |
      Enter the value for the left hand side of the comparison
	  
      This can contain other `%variables%`{lang=cs} as well as inline functions
  - name: Operator
    type: Select
    required: true
    default: Equals
    description: |
      Choose the type of comparison to perform

      - `Equals`: Check if the variable equals a given value
      - `Not Equals`: Check if the variable does not equal a given value
      - `Less Than`: Check if a numeric variable is less than a given value (does NOT include the set value)
      - `Greater Than`: Check if a numeric variable is greater than a given value (does NOT include the set value)
  - name: Value
    type: Text
    required: true
    description: |
      Enter the value for the right hand side of the comparison

      This can contain other `%variables%`{lang=cs} as well as inline functions
  - name: Auto Type
    type: Toggle
    default: false
    description: |
      By default, values which have not already been typed are treated as text, or `string`{lang=cs} variables.

      Enable `Auto Type` to automatically determine the type for the variable value.

      For example:
      - `0`{lang=cs} can be auto-typed to a numeric type such as `int`{lang=cs} or `long`{lang=cs}
      - `true`{lang=cs} or `false`{lang=cs} can be auto-typed to a `bool`{lang=cs}
  - name: Ignore Case
    type: Toggle
    default: false
    description: |
      Whether or not the comparison will be performed without checking casing
	  
      For example:
      - `yes`{lang=cs} would match `YES`{lang=cs} is it is checked
      - `yes`{lang=cs} would not match `YES`{lang=cs} if it is not checked
---

