---
title: OBS Studio
description: Configure Streamer.bot to interact with your OBS Studio instances
logo: https://streamer.bot/img/integrations/obs.svg
---

:wip

## Overview
> **Streamer.bot supports both OBS WebSocket versions, *v4.9+*{.obs-version-badge} and *v5+*{.obs-version-badge}**
This documentation refers to OBS WebSocket version *v5+*{.obs-version-badge}
{.is-info}

Adding at least one OBS connection will allow Streamer.bot to control your OBS.

![overview](/broadcasters/obs/overview.png =1000x)

Once configured, connected OBS sessions will report their status on this screen.

## Configuration
With v28+ OBS Websocket is pre-installed, so you don't need to install it. If you can't see it under tools you might need to do a `Help` --> `Check File Integrity` in OBS. After that it should show up.

- [<img src="/logos/obs-websocket.png"/>**Download OBS WebSocket (OBS v27 and earlier)*<i class="mdi mdi-github"></i> obs-websocket v5+***](https://github.com/obsproject/obs-websocket/releases/tag/5.0.1)
{.btn-grid .my-5}

<kbd>Right-Click</kbd> <kbd>-></kbd> <kbd>Add</kbd> to define a new OBS connection

![connection](/broadcasters/obs/obs-connection.png =250x)

### Name
Enter any name or label to describe this OBS instance, e.g. `Local`

### Version
Select the version of OBS WebSocket to use for this connection.

> **Warning**
> As of OBS Studio v28.0, OBS WebSocket v5+ is included by default.
> To continue using OBS WebSocket v4.9+, you must install the *obs-websocket-4.9.1-compat*{.obs-version-badge} plugin
{.is-warning}

It is recommended to update to *v5+*{.obs-version-badge} if you are currently using an older version.

### Host
Default is localhost, `127.0.0.1`
To connect to another OBS instance on your local network, you can enter the local IP address, e.g. `192.168.1.10`

### Port
Default is: *v4.9+*{.obs-version-badge} = `4444` or *v5+*{.obs-version-badge} = `4455`
It's recommended to keep this the same unless you are using multiple OBS portable installs on your same desktop.

### Password
Not required, devices can only connect to your OBS if they're on the same network as you.

### Auto Connect on Startup
When toggled this auto connects your OBS connection when you launch streamer.bot.

### Reconnect on Disconnect
When toggled this tries to reconnect (by default every 30s) when streamer.bot loses connection with your OBS.

### Retry Interval
When Streamer.bot loses connection with your OBS this by default will try to reconnect every 30s, but you can change it to what you want.

## Status Panel
Overview of connection information available on the right-hand panel{.subtitle}

### OBS Information
Shows the version number of OBS and the installed WebSocket plugin

### Current Scene
Shows the name of the currently broadcasting scene on that connection

### Stream Status
Shows the status of current streaming and recording activity

### Sources
Lists all sources present on the currently selected scene

## Events
Select an OBS connection in the top panel, then <kbd>Right-Click</kbd> <kbd>-></kbd> <kbd>Add</kbd> in the bottom events panel to register an OBS event.

![add obs event currentprogramscenechanged](/broadcasters/obs/add-obs-event-currentprogramscenechanged.png =300x)

### Event
Select the event type from OBS

A reference of all OBS Studio events is available [here](/Broadcasters/OBS/Events)

### Group
Optional group name to keep your events organized

### Action
Select the action to be executed any time the selected event is fired off from OBS

## Connect/Disconnect Actions
Events emitted when the OBS websocket server has connected/disconnected{.subtitle}
* [**Connected *OBS Websocket has connected*** *v0.1.15*{.version-badge}](/Broadcasters/OBS/Actions/Connected)
* [**Disconnected *OBS Websocket has disconnected*** *v0.1.15*{.version-badge}](/Broadcasters/OBS/Actions/Disconnected)
{.btn-grid .list .dense .my-5}

***

### OBS Raw
- [<i class="mdi mdi-code-json text--obs"></i>**OBS Raw *Sub-Action for executing raw OBS requests***](/Sub-Actions/OBS/Raw)
{.btn-grid .my-5}

### OBS Raw Requests
- [<i class="mdi mdi-frequently-asked-questions
 text--obs"></i>**OBS Raw Requests *Reference of all requests supported with OBS Raw***](/Broadcasters/OBS/Requests)
{.btn-grid .my-5}