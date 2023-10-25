---
title: Version 0.0.52
description: 
published: true
date: 2023-06-11T15:08:20.446Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:11.986Z
---

Visit the main update for [Streamer.bot 0.0.50](/Changelogs/Archives/Version-0050) to see all the shiny new features and updates. Also see [Streamer.bot 0.0.51](/Changelogs/Archives/Version-0051) for more fixes

Since I forgot to update the Twitch client keys in the initial release, this version will request a re-authorization to twitch.

* Miscellaneous fixes
* Hopefully final fix for BTTV/FFZ emotes
* Fix Action Queue UI not working
* Fix issues with Bot login
{.changelog-fixes}

<span></span>

* WebSocket Server events have been re-worked, read [here](#websocket-server-events) for more info
{.changelog-updates}

<span></span>

* Add new `Does Not Exist` operator for the if logic Sub-Action
* Did someone say, [StreamElements](#streamelements) support?
{.changelog-new}

## Twitch accounts re-authorization
To re-authorize both accounts, the easiest way is to use 2 different browsers, connect your main account using your default browser, then change the default browser to another one, login with your bot account, and then authorize the bot account.

## StreamElements!
You can now connect to your StreamElements account and get tip events. To configure this, you will need to obtain your JWT token, and set this within the settings. There is no sign in authorization to do this at the moment due to how long it takes to get this approved.

1 new event is added for StreamElements, and they are also included in the Websocket broadcast

This capability is experimental, its very hard to test for StreamElements, I would need more data, specifically debug logging of someone using it and receiving events to be able to extend its capabilities.

## WebSocket Server Events
Given there there are now 53 events that can be broadcast over the webserver socket, I thought it best to change this to a subscription type setup, so that way each socket can control its own events it receives.

For more information see [WebSocket Server Events](/Servers-Clients/WebSocket-Server/Events)