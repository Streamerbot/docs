# Renamed
File/Folder Watcher renamed trigger.

## Details
This event triggers when a selected file/folder gets renamed.

- `Using a file`: this triggers when the file is renamed.
- `Using a folder`: this triggers when a file from this folder gets renamed.

## Parameters
### `Watcher`
Select any or a specific watcher from the `Settings -> File/Folder Watcher` tab

## Variables
:variables-description

Name | Description
----:|:------------
`watcherFolder` | The folder you're watching for changes e.g. `C:\Desktop\Example-Folder`
`watcherFilter` | The filter of this watcher e.g. `*.*`
`oldFullPath` | The previous full path e.g. `C:\Desktop\Example-Folder\Example.txt`
`oldFilename` | The previous full file name e.g. `Example.txt`
`fullPath` | The full path of the file e.g. `C:\Desktop\Example-Folder\Example-2.txt`
`fileName` | The full file name including the file extension e.g. `Example-2.txt`
`changeType` | The change type e.g. `Renamed`