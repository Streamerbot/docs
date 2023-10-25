---
title: Command Triggered
description: Commands Triggers Reference
published: true
date: 2023-03-16T10:31:13.687Z
tags: 
editor: markdown
dateCreated: 2023-03-14T16:25:18.117Z
---

## Overview
This triggers when someone uses your command.

For a detailed guide on how Commands work in Streamer.bot see [this page](/Commands).

## Configuration
### Commands
Select a command from the Commands tab.

## Variables
Name | Description
----:|:------------
`command` | The command that was used
`commandId` | The ID of the command
`commandSource` | The command source <br> `twitch`/`youtube`
`commandType` | The type of the command e.g. `message`
`msgId` | The unique message id for this message
`rawInput` | The message entered, if the command was a Starts With, this will be removed 
`rawInputEscaped` | The message escaped
`rawInputUrlEncoded` | The message URL encoded
`input#` | The # word of the message entered, spaces are delimiters and variable names are 0 indexed, so `input0` would give the first word, `input1` would give the second, and so on
`inputEscaped#` | The indexed word escaped
`inputUrlEncoded#` | The indexed word URL encoded
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`counter` | A running total of how many times a command has been run since application launch (if `Persisted` is checked, the total will be saved and reloaded at launch)
{.vars-table}

> These variable include the [User Variables](/Variables/User-Variables) and the [Broadcaster Variables](/Variables/Broadcaster)
{.is-success}

---

- [<i class="mdi mdi-chevron-left"></i>**Commands Triggers Reference *Go Back***](/Triggers/Core/Commands)
- [<i class="mdi mdi-clock-alert primary--text"></i> **Command Cooldown *Up Next***](/Triggers/Core/Commands/Command-Cooldown)
{.btn-grid .my-5}