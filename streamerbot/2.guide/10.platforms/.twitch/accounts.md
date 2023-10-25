---
title: Twitch Accounts
description: Set up your Broadcaster and Bot accounts for Streamer.bot to interact with Twitch
published: true
date: 2023-03-27T18:36:00.251Z
tags: twitch
editor: markdown
dateCreated: 2021-08-25T21:32:56.848Z
---

![connect_to_twitch_.png](/quick-start/connect_to_twitch_.png =800x)

## Broadcaster Account

If you want streamer.bot to be able to monitor chat and Twitch! events, a `Broadcaster` account must be defined

Press `Connect to Twitch` to automatically obtain a token

`Auto Connect` will set streamer.bot to connect to twitch with the defined account on startup

`Auto Reconnect` instructs streamer.bot to attempt reconnection in the case of any network interruption to the platform

***

## Bot Account

By default any [sub-actions](/Sub-Actions#main) will be sent through the Broadcaster account. If you want a secondary account to send these actions / messages it can be defined here in the same way

::callout{color=amber icon=i-mdi-alert}
Sending whispers programatically is something that `Twitch` restricts fairly heavily.
If the chosen account is not more than **12** months old, or already pre-verified as a **bot** you will not be able to send whispers from the application
::

::callout{color=green icon=i-mdi-check-circle}
If you do not intend to use a bot account, leave this field blank or you will restrict certain actions from working correctly such as responding to chat commands that the bot has written in chat
::

Once you have a bot account configured, you can select which account should send chat messages on a per [sub-actions](/api/sub-actions) level.


## Refresh Categories

Use this to pull a current list of available Twitch categories. These can be used as variables in [sub-actions](/api/sub-actions) for example to change scene if category is changed to a specific game