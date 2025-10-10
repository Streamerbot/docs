---
title: Folder Exists
description: Determines if a given folder exists
version: 1.0.1
parameters:
  - name: Folder to Check if Exists
    type: File
    required: true
    description: Select the folder to check, or enter a path
  - name: Variable Name
    type: Text
    default: folderExists
    description: The variable name to contain the result.
variables:
  - name: folderExists
    type: bool
    description: `True` if the folder exists, `False` if it doesn't.
---
