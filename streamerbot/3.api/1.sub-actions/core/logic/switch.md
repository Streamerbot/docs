---
title: Switch
description: Allows for multi-way branching based on the value of an expression
version: 1.0.0
parameters:
  - name: Input
    type: Text
    required: true
    description: |
      Enter the value for the left hand side of the comparison, this input supports full variable parsing and inline functions
  - name: Auto Type
    type: Toggle
    default: false
    description: |
      By default, values which have not already been typed are treated as text, or `string`{lang=cs} variables.

      Enable `Auto Type` to automatically determine the type for the variable value.

      For example:
      - `0`{lang=cs} can be auto-typed to a numeric type such as `int`{lang=cs} or `long`{lang=cs}
      - `true`{lang=cs} or `false`{lang=cs} can be auto-typed to a `bool`{lang=cs}
---

You can add any number of cases to a switch by right clicking on the `switch` Sub-Action and selecting "Add Case"
![Switch Sub-Action context menu showing "Add Case" option](assets/switch-add-case-context-menu.png)

You can add one or more values to a case.  If any of the case's values match the `switch` input, that case will be run.
![Add Case Dialogue](assets/switch-add-case-dialogue.png)

::note
Only the first matching case will be run

If no cases match, the `default` case will be run
::