---
title: Get Team Info For Target
description: Twitch Sub-Actions Reference
published: true
date: 2022-11-04T15:33:18.272Z
tags: 
editor: markdown
dateCreated: 2022-11-03T19:34:41.017Z
---

## Overview
Collects follow data from a Twitch user.

![overview.png](/Sub-Actions/Twitch/get-team-info-for-target/overview.png =400x)

## Configuration
### Source Type
Name | Description
----:|:------------
`Broadcaster` | The broadcast user.
`User` | User that invoked the action e.g. a raid leader, subscriber, point redeemer etc.
`From Input` | This will take the next word proceeding the trigger as the username to lookup. This user does not have to be present in the channel
`Variable` | Use the content of an existing variable as the target

### Variable
If you selected `Variable` as your `Source Type`, enter the name of the variable you would like to read in.

## Variables
Name | Description
----:|:------------
`teamId#` | The id of the target's team.
`teamName#` | The name of the target's team.
`teamDisplayName#` | The display name of the target's team.
`teamBackgroundUrl#` | The background url of the target's team.
`teamBannerUrl#` | The banner url of the target's team.
`_jsonTeamData` | The json, used for coding in C#.

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Sub-Actions *Go Back***](/Sub-Actions/Twitch)
{.btn-grid .my-5}