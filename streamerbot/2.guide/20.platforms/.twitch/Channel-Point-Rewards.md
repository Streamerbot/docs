---
title: Channel Point Rewards
description: Twitch Events Reference
published: true
date: 2023-03-27T18:36:00.251Z
tags: twitch, channel-points
editor: markdown
dateCreated: 2021-08-25T21:31:18.137Z
---

## Overview

**Streamer.bot** can automatically execute [Actions](/Actions) when a Channel Point Reward is redeemed

When the `Broadcaster` account is connected, **Streamer.bot** will automatically pull a list of available rewards from the Twitch profile and actions can be assigned to them immediately. 

You can also `Add` and `Delete` rewards directly from the application. 

> It is **highly recommended** to create your rewards through Streamer.bot
> This gives Streamer.bot full control of the reward and is **required** for many of the features outlined below.
{.is-warning}

## Guide
To create a new reward <kbd>Right-Click</kbd> inside the Channel Point Rewards panel and click `Add`

![New Channel Point Reward](/119646229-d4949f80-be16-11eb-806f-8dca85bdce45.png)

### Title
The name of the reward

`Enabled` The reward is visible to the channel

`Paused` The reward can not be redeemed but can be seen if `Enabled` is also checked

### Cost
The number of channel points needed to redeem this reward

`User Input Required` This will show a text box to the user to allow them to enter a message. This can be read by [sub-actions](/Sub-Actions#main) with the `%rawInput%` variable

### Prompt
This is the text that will be displayed to the user before they confirm redemption to explain what will happen

`Background Colour` Sets the colour of the button

`Redemption Skips Queue` Tells the [action](/Actions) to ignore the `Blocking` flag on the [action queue](/Settings/General#action-queues) assigned to that action

`Max per stream` & `Max per User per Stream` Defines limits on how many times this reward can be redeemed in any one stream

`Global Cooldown` Defines the miniimum time in seconds before this reward can be redeemed again by anyone

### Counters
Actions in **Streamer.bot** have per-session and per-command variables `%counter%`, and `%userCounter%` that records how many times that channel reward has been used. 

By default this clears when the application is closed but the following options will save the counts to a file so they will persist between sessions

`Persist Counter` Will save the total number of executions for this command

`Persist per User Counter` Will save details of how often each user has executed this command

### Action
`Action` Defines the action that will be executed when the reward is redeemed

## Variables
The following variables will be available after a channel point redemption:

Name | Description
----:|:------------
`redemptionId` | String identifier for this redemption (used to refund reward) <br> `4d9f236b-7486-481a-89af-1d03676d5275`
`rewardId` | String identifier for this reward <br> `44e86f71-8ace-4739-a123-3ff095489343`
`rewardName` | Name of the reward <br> `My Reward`
`rewardPrompt` | The verbiage shown on the channel point description *v0.1.5+*{.version-badge} <br> `My cool Reward Prompt`
`rewardCost` | The channel point cost of the redeemed reward *v0.1.5+*{.version-badge}  <br> `100`
`counter` | Number of times this reward has been redeemed <br> `1`
`userCounter` | Number of times the same user has redeemed this reward <br> `1`
`rawInput` | String text entered by the user (if required) <br> `https://streamer.bot/Test Unescaped Text $$$`
`rawInputEscaped` | String text entered by the user (escaped) <br> `https://streamer\.bot/Test Escaped Text \$\$\$`
`user` | The user that had redeemed the channel point
`userName` | User login name <br> *e.g. on Twitch this is the username in all lowercase, useful for comparison*
`userId` | Unique user identifier
`userType` | Specifies which streaming service the triggering user is coming from *v0.1.8+*{.version-badge} <br> `twitch` or `youtube`
`isSubscribed` | Boolean value indicating the sender's subscription status <br> `True`/`False`
`isModerator` | Boolean value indicating the sender's moderator status <br> `True`/`False`
`isVip` | Boolean value indicating the sender's VIP status <br> `True`/`False`
{.vars-table}

> This will also include all the [Broadcaster Variables](/Variables/Broadcaster)
{.is-success}

---

- [<i class="mdi mdi-chevron-left"></i>**Twitch Events *Go Back***](/Platforms/Twitch/Events)
{.btn-grid .my-5}