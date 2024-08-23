---
title: Read Lines From File
description: Load the contents of a file into variables
parameters:
  - name: File to read from
    type: File
    required: true
    description: Select the file to load, or enter a path
  - name: Variable Name
    type: Text
    default: line
    description: Enter a variable name to override the default `line#` variables with your own naming scheme
  - name: Parse Variables
    type: Toggle
    default: false
    description: Enable this option to enable parsing and replacement of `%variables%`{lang=cs} found within the file contents
  - name: Attempt auto-typing
    type: Toggle
    default: false
    description: |
      While reading the contents of the file, attempt to auto-type on a line-by-line basis.

      For example, if a line consists of a number, the resulting variable for that line can be properly typed as an `int`{lang=cs}
variables:
  - name: lineCount
    type: int
    description: Total number of lines in the file
    value: 12
  - name: 'line#'
    description: |
      Each line of output parsed from the file parsed to its own variable

      e.g. `%line0%`{lang=cs}, `%line1%`{lang=cs}, `%line2%`{lang=cs}, and so on...
    value: 'Hello, world!'
  - name: fileFound
    type: bool
    description: |
      `True` or `False` if the file is present on disk
---
