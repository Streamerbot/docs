---
title: Deleted
description: File/Folder Watcher Triggers Reference
published: true
date: 2023-03-16T11:04:31.290Z
tags: 
editor: markdown
dateCreated: 2023-03-14T21:45:58.861Z
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
`changeType` | The change type e.g. `Deleted`
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**File/Folder Watcher Triggers Reference *Go Back***](/Triggers/Core/File-Folder-Watcher)
- [<i class="mdi mdi-rename-box primary--text"></i> **Renamed *Next Up***](/Triggers/Core/File-Folder-Watcher/Renamed)
{.btn-grid .my-5}