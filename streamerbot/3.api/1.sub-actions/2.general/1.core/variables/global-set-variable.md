---
title: Set Global Variable
description: Logic Sub-Action Reference
published: true
date: 2023-04-10T05:37:55.834Z
tags: 
editor: markdown
dateCreated: 2022-10-19T05:56:41.484Z
---

## Overview
![logic-global-set.png](/logic-global-set.png =400x)

## Configuration
### Destination

This sub-action stores data in one of the `Global` data stores, valid options are `Global` & `User`
`User` context is further subdivided into `Redeemer` & `Target`

User Context | Description
-----|-----
`Redeemer`| Store data for the user activating the action
`Target`| Store data for the current `targetUser` - Used in conjunction with the [Get Info for Target](/Sub-Actions/Twitch/Get-User-Info-for-Target) sub-action

### Persisted

Data can be stored in a `Temporary` store or a `Persisted` store. Persisted data will be saved to the `Globals.dat` file in the `Data` folder. Data saved in this way will survive application restarts. 

### Variable Name

This is the name of the `Global` / `User` variable to write to
> This should always be in `camelCase` ie. with a lower case initial letter, Streamer.bot can not retrieve data from any store if the initial letter is capitalised
{.is-warning}

### Content

The final line provides space to define what to store in the named `Global`
This has 3 modes:

Mode | Description
-----|-----
`Value`| Store the entered value, exactly as written 
`Increment`| Take the current global value and add the specified value to it (only works for integers)
`Argument` | Store the contents of a named active argument (do not include the % symbols)

---

- [<i class="mdi mdi-chevron-left"></i> **Globals Sub-Actions Reference *Go Back***](/Sub-Actions/Globals)
- [<i class="mdi mdi-earth primary--text"></i> **Global (Get) *Next Up***](/Sub-Actions/Globals/Get-Global-Variable)
{.btn-grid .my-5}