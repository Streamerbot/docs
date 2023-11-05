---
title: Get Global Variable
description: Globals Sub-Action Reference
published: true
date: 2023-04-10T05:37:44.629Z
tags: 
editor: markdown
dateCreated: 2022-10-19T05:54:26.112Z
---

## Overview
This sub-action copies data from a stored `Global` type variable into a custom `Argument` so it is available to the rest of the action.

![logic-global-get.png](/logic-global-get.png =400x)

## Configuration
### Source
Global variables can be stored with or without an associated `userID`
`Global` source are single variables that have the same data no matter the user context

`User` source stores a copy of that variable name against each unique user so when data is retrieved it will pull based on the selected context:

User Context | Description
-----|-----
`Redeemer`|Pull the information for the user activating the action
`Target`|Pull the information for the current `targetUser` - Used in conjunction with the [Get Info for Target](/Sub-Actions/Twitch/Get-User-Info-for-Target) sub-action


### Persisted
Any Global / User variable can be set as `Persisted`. If this flag is set Streamer.bot will save the data into the `Globals.dat` file in the `Data` folder. Data saved in this way will survive application restarts. 
When fetching data you can select to use the persisted data store or the temporary one. 
> These data stores are completely separate so data stored in the `Persisted` memory will not be copied to the `Temporary`. Generally speaking you will always want to match your data store
{.is-warning}

### Variable Name
This is the name of the `Global` / `User` variable to fetch
> This should always be in `camelCase` ie. with a lower case initial letter, Streamer.bot can not retrieve data from any store if the initial letter is capitalised
{.is-warning}

### Destination Variable
This is the name of the custom `Argument` the data will be stored in.
> It is best practice to always name this something different than the `Global` you are reading from. Not only does this make your workflow easier to read and debug, it can also prevent strange issues with logic and inline functions
{.is-success}

### Default Value
If the specified `Global` / `User` variable does not exist for that context, the Get subaction will create it for you and populate with this value

---

- [<i class="mdi mdi-chevron-left"></i> **Globals Sub-Actions Reference *Go Back***](/Sub-Actions/Globals)
- [<i class="mdi mdi-earth primary--text"></i> **Global (Set) *Next Up***](/Sub-Actions/Globals/Set-Global-Variable)
{.btn-grid .my-5}