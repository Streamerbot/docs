---
title: Read Random Lines From File
description: Load the contents of a file and populate a set of variables from random lines
parameters:
  - name: File to read from
    type: File
    required: true
    description: Select the file to load, or enter a path
  - name: Variable Name
    type: Text
    default: line
    description: Enter a variable name to override the default `randomLine#` variables with your own naming scheme
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
  - name: Count
    type: Number
    default: 1
    description: Number of random lines to extract from the file
variables:
  - name: 'randomLine#'
    description: |
      Each random line extracted based on the `Count` you configured. The line counter suffix is omitted from the first line read.

      e.g. `%randomLine%`{lang=cs}, `%randomLine1%`{lang=cs}, `%randomLine2%`{lang=cs}, and so on...
    value: 'Hello, world!'
  - name: 'randomLineNumber#'
    type: int
    description: |
      The line number (numbered from 0) of each random line read. The line counter suffix is omitted from the first line number.

      e.g. `%randomLineNumber%`{lang=cs}, `%randomLineNumber1%`{lang=cs}, `%randomLineNumber2%`{lang=cs}, and so on...
    value: 3
  - name: fileFound
    type: bool
    description: |
      `True` or `False` if the file is present on disk
---
