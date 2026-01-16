---
title: File Tail Changed
navigation.title: Changed
description: Trigger for a Change from a File Tail
version: 0.2.3
parameters:
  - name: Watcher
    type: Select
    description: |
      Select a file tail from the Services -> File Tails tab.

      - Select `Any` to trigger on **any file tail**

      ::tip
      You can quickly register a new file tail by clicking the `Create File Tail` button!
      ::
variables:
  - name: filePath
    type: string
    description: The file path
  - name: fileName
    type: string
    description: The file name
  - name: line
    type: string
    description: The line of the file tail
---
