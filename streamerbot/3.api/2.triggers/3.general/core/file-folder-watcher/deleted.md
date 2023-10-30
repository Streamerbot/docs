# Deleted
File/Folder Watcher deleted trigger.

## Details
This event triggers when a selected file/folder gets deleted.

- `Using a file`: this triggers when the file is deleted.
- `Using a folder`: this triggers when a file from this folder gets deleted.

## Parameters
### `Watcher`
Select any or a specific watcher from the `Settings -> File/Folder Watcher` tab

## Variables
:variables-description

Name | Description
----:|:------------
`watcherFolder` | The folder you're watching for changes e.g. `C:\Desktop\Example-Folder`
`watcherFilter` | The filter of this watcher e.g. `*.*`
`fullPath` | The full path of the file e.g. `C:\Desktop\Example-Folder\Example.txt`
`fileName` | The full file name including the file extension e.g. `Example.txt`
`changeType` | The change type e.g. `Deleted`