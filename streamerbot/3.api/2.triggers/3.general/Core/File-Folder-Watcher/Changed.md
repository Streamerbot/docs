---
title: Changed
description: File/Folder Watcher Triggers Reference
published: true
date: 2023-03-16T11:04:00.410Z
tags: 
editor: markdown
dateCreated: 2023-03-14T21:51:02.377Z
---

## Overview
This triggers when a file gets created in the folder you're watching.

For a detailed guide on how the File/Folder Watcher works in Streamer.bot see [this page](/Settings/File-Folder-Watcher).

## Configuration
### Watcher
Select any or a specific watcher from the Settings --> File/Folder Watcher tab

## Variables
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
{.vars-table}

> Change the `#` to a number from 0 to the end of the lines. So e.g. `%line0%`, `%line1%`, `%line2%`
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**File/Folder Watcher Triggers Reference *Go Back***](/Triggers/Core/File-Folder-Watcher)
- [<i class="mdi mdi-creation primary--text"></i> **Created *Next Up***](/Triggers/Core/File-Folder-Watcher/Created)
{.btn-grid .my-5}