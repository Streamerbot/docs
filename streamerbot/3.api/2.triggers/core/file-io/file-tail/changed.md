---
title: Changed
description: Trigger for a Change from a File Tail
version: 0.2.3
variables:
  - name: filePath
    type: string
    description: The file path
  - name: fileName
    type: string
    description: The fill name
  - name: line
    type: string
    description: The line of the file tail
---

:image-preview

## Parameters
::field-group
  ::field{name=Watcher type=Select}
    Select a file tail from the Settings -> File Tails tab.

    - Select `Any` to trigger on **any file tail**

    ::tip{color=amber}
    You can quickly register a new file tail by clicking the `Create File Tail` button!
    ::
  ::
::