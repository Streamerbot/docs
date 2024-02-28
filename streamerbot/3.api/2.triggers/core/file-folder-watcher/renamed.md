---
title: Renamed
description: Trigger for when a File/Folder Watcher is Renamed
variables:
  - name: watcherFolder
    type: string
    description: The folder you're watching for changes
    value: C:\Desktop\Example-Folder
  - name: watcherFilter
    type: string
    description: The filter of this watcher
    value: '*.*'
  - name: oldFullPath
    type: string
    description: The old full path of the file
    value: 'C:\Desktop\Example-Folder\Old-Example.txt'
  - name: oldFilename
    type: string
    description: The old full file name including the file extension
    value: Old-Example.txt
  - name: fullPath
    type: string
    description: The full path of the file
    value: 'C:\Desktop\Example-Folder\Example.txt'
  - name: fileName
    type: string
    description: The full file name including the file extension
    value: Example.txt
  - name: changeType
    type: string
    description: The change type
    value: Renamed
---

:image-preview

## Parameters
::field-group
  ::field{name=Watcher type=Select}
    Select a watcher from the Settings -> File/Folder Watcher tab.

    - Select `Any` to trigger on **any watcher**

    ::tip{color=amber}
    You can quickly register a new watcher by clicking the `Create File Watcher` button!
    ::
  ::
::

## Details
- `Using a file`: this triggers when the content of a selected file changes.
- `Using a folder`: this triggers when a file from the selected folder changes.