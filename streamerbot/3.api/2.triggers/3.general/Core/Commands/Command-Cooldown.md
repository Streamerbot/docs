---
title: Command Cooldown
description: Commands Triggers Reference
published: true
date: 2023-03-16T10:32:02.350Z
tags: 
editor: markdown
dateCreated: 2023-03-14T16:24:24.254Z
---

## Overview
This triggers when your command is on a cooldown and someone tries to use it.

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
`cooldownLeft` | How many seconds are left for the cooldown, and is the maximum of the global and user cooldown left
`globalCooldownLeft` | How many seconds are left for the global cooldown of the command
`userCooldownLeft` | How many seconds are left for the user cooldown of the command
{.vars-table}

> These variable include the [User Variables](/Variables/User-Variables) and the [Broadcaster Variables](/Variables/Broadcaster)
{.is-success}

---

- [<i class="mdi mdi-chevron-left"></i>**Commands Triggers Reference *Go Back***](/Triggers/Core/Commands)
- [<i class="mdi mdi-comment-alert primary--text"></i> **Command Triggered *Up Next***](/Triggers/Core/Commands/Command-Triggered)
{.btn-grid .my-5}