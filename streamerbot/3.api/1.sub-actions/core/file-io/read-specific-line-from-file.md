---
title: Read Specific Line From File
description: Populate a variable with the contents of a specific line from a file
parameters:
  - name: File to read from
    type: File
    required: true
    description: Select the file to load, or enter a path
  - name: Variable Name
    type: Text
    default: line
    description: Enter a variable name to override the default `line` variable
  - name: Parse Variables
    type: Toggle
    default: false
    description: Enable this option to enable parsing and replacement of `%variables%`{lang=cs} found within the file contents
  - name: Attempt auto-typing
    type: Toggle
    default: false
    description: |
      While reading the contents of the file, attempt to auto-type on a line-by-line basis.

      For example, if a line consists a number, the resulting variable for that line can be properly typed as an `int`{lang=cs}
  - name: Line Number
    type: Number
    default: 1
    description: The line to extract from the file, numbered from 1
variables:
  - name: 'line'
    description: |
      Contents of the selected line from the file
    value: 'Hello, world!'
  - name: fileFound
    type: bool
    description: |
      `True` or `False` if the file is present on disk
---
