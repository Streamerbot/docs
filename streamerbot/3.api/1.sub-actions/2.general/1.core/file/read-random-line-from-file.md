---
title: Read Random Lines From File
description: File Sub-Actions Reference
published: true
date: 2023-04-23T19:47:17.270Z
tags: 
editor: markdown
dateCreated: 2021-11-18T21:44:05.986Z
---

## Overview
Using this sub-action, you can load the entire contents of a file into your action, then you can have the bot read a random line from the file and load it into a variable `%randomLine%`.

![sub-action-readrandomlinefromfile-01.png](/sub-action-readrandomlinefromfile-01.png =400x)

## Configuration
### Parse Variables
If this option is selected, when reading in the lines, if there are any %variables% present, they will be replaced with the current contents of the specified variable. 
Example:

You have a file containing a list of welcome messages, such as: 
Welcome `%user%`.
Greetings `%user%`.
Nice to see you `%user%`, have a seat.

The `%user%` would be replaced when reading the file.

### Attempt Auto-typing
While reading the contents of the file, an attempt will be made on each line to determine its ‘type’. So, if it's a number, it will make sure the variable is defined as a numeric, if it contains a string it will define the variable as a string. This is useful for future operations on the created variable.

### Count
This option defines the number of lines that will be read from the file.

---

- [<i class="mdi mdi-chevron-left"></i> **File Sub-Actions *Go Back***](/Sub-Actions/File)
{.btn-grid .my-5}