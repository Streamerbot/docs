---
title: Write To File
description: Write variable data to a specified file
parameters:
  - name: File to write to
    type: File
    required: true
    description: Select a file, or enter a path
  - name: Append to file
    type: Toggle
    default: false
    description: Append to the existing file contents rather than overwriting
  - name: Text to write
    type: Text
    description: |
      Enter the text to write to the file, this can include variables
---
