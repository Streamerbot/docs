# File Watcher
### Tab {.tabset}
#### Changed
Only `lines` or `data` will exist for a changed event, not both.
```json
{
  "fullPath": "", /* full path to the file that changed */
  "fileName": "", /* file name of the file that changed */
  "name": "", /* file name without extension of the file that changed */
  "lines": [ /* list of string of the contents of the file, line by line, if it has not been parsed as a json */
  ],
  "data": { /* json parsed contents of file, only top level key value pairs */
    "key": "value"
  }
}
```

#### Created
```json
{
  "fullPath": "", /* full path to the file that changed */
  "fileName": "", /* file name of the file that changed */
  "name": "", /* file name without extension of the file that changed */
}
```

#### Deleted
```json
{
  "fullPath": "", /* full path to the file that changed */
  "fileName": "", /* file name of the file that changed */
  "name": "", /* file name without extension of the file that changed */
}
```