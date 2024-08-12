---
title: Get Input
description: Spawn a dialog to interactively retrieve user input
parameters:
  - name: Title
    type: Text
    required: true
    description: Enter the title for the dialog box
  - name: Prompt
    type: Text
    required: true
    description: Enter the prompt text for the dialog box
  - name: Original Text
    type: Text
    description: Optionally enter a default value for the input box
  - name: Output Variable
    type: Text
    required: true
    default: inputResult
    description: Enter the name of the variable you'd like to populate with the user input
  - name: Auto Type Output
    type: Toggle
    default: False
    description: |
      By default, all values are treated as text, or `string`{lang=cs} variables.

      Enable `Auto Type` to automatically determine the type for the entered value.

      For example:
      - `0`{lang=cs} can be auto-typed to a numeric type such as `int`{lang=cs} or `long`{lang=cs}
      - `true`{lang=cs} or `false`{lang=cs} can be auto-typed to a `bool`{lang=cs}
variables:
  - name: success
    type: bool
    description: |
      if `Ok` was pressed, then `true`{lang=cs}, else `false`{lang=cs} if canceled or closed
    value: true
  - name: <inputResult>
    description: Variable name and type are dependent on the configured `Output Variable` and `Auto Type` options
---

## Preview
![preview](assets/get-input-preview.png)