---
title: File Exists
description: Determines if a given file exists
version: 1.0.1
parameters:
  - name: File to Check if Exists
    type: File
    required: true
    description: Select the file to check, or enter a path
  - name: Variable Name
    type: Text
    default: fileExists
    description: The variable name to contain the result.
variables:
  - name: fileExists
    type: bool
    description: `True` if the file exists, `False` if it doesn't.
---
