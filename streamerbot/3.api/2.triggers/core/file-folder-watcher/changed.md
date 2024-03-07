---
title: Changed
description: Trigger for when a File/Folder Watcher is Changed
variables:
  - name: watcherFolder
    type: string
    description: The folder you're watching for changes
    value: 'C:\Desktop\Example-Folder'
  - name: watcherFilter
    type: string
    description: The filter of this watcher
    value: '*.*'
  - name: fullPath
    type: string
    description: The full path of the file
    value: 'C:\Desktop\Example-Folder\Example.txt'
  - name: fileName
    type: string
    description: The full file name including the file extension
    value: Example.txt
  - name: fileSize
    type: number
    description: The file size in bytes
    value: 1 MB > 1000000 bytes
  - name: changeType
    type: string
    description: The change type
    value: Changed
  - name: empty
    type: boolean
    description: Is the file empty?
    value: True
  - name: lineCount
    type: number
    description: The total number of lines
    value: 1
  - name: line#
    type: string
    description: Each line of the file
    value: Hello World!
  - name: lineEscaped#
    type: string
    description: Each line of the file escaped for URL's
    value: Hello%20World%21
---

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