---
title: Read Specific Line From File
description: File Sub-Actions Reference
published: true
date: 2023-03-21T13:54:27.441Z
tags: 
editor: markdown
dateCreated: 2023-03-21T13:54:00.555Z
---

## Overview
With this Sub-Action you can read a specific line of a file.

![read-specific-line-from-file.png](/read-specific-line-from-file.png =400x)

## Configuration
### Parse Variables
If this option is selected, when reading in the lines, if there are any `%variables%` present, they will be parsed for you.

For example, you have a file of welcome messages, that consist of `Welcome %user%`, with variations on that, the `%user%` would be replaced when reading the file.

### Attempt Auto-typing
While reading the contents of the file, an attempt will be made on each line to auto-type it.  So if it's a number, it will make sure the variable contains a number type.

## Variables
Name | Description
----:|:------------
`line` | The contents of that line
`fileFound` |  This can be used to see if the file is present. Returns true or false.

---

- [<i class="mdi mdi-chevron-left"></i> **File Sub-Actions *Go Back***](/Sub-Actions/File)
{.btn-grid .my-5}