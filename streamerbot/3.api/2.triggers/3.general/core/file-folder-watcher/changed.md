# Changed
File/Folder Watcher changed trigger.

## Details
This event triggers when a selected file/folder changes.

- `Using a file`: this triggers when the content of the file changes.
- `Using a folder`: this triggers when a file from this folder changes.

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
`fileSize` | The file size in bytes e.g. with 100 bytes the value is: `100`
`changeType` | The change type e.g. `Changed`
`empty` | If the file is empty or not e.g. `True`/`False`
`lineCount` | The total number of lines e.g. `1`
`line#` | Each line of the file
`lineEscaped#` | Each line of the file escaped for URL's