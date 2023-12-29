---
title: Add Random Users
description: Twitch Sub-Actions Reference
published: true
date: 2023-01-20T16:58:02.551Z
tags: 
editor: markdown
dateCreated: 2022-11-03T19:36:10.528Z
---

## Overview
Get a custom amount of random users.

![overview.png](/Sub-Actions/Twitch/add-random-users/overview.png =400x)

## Configuration
### Count
The amount of random users that you want to use.

### Present Only
Only selects random users that are present.

## Variables
`#` starts at `0`, e.g. if the Count is set to `50` the `#` will be `0`, `1`, `2` ...... `47`, `48`, `49`.

Name | Description
----:|:------------
`randomUser#` | The random user's display name.
`randomUserName#` | The random user's login name.
`randomUserId#` | The random user's id.
{.vars-table}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}