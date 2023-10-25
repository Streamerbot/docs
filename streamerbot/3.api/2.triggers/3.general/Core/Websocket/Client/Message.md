---
title: Message
description: WebSocket Client Triggers Reference
published: true
date: 2023-03-16T22:04:07.074Z
tags: 
editor: markdown
dateCreated: 2023-03-16T22:03:09.481Z
---

## Overview
The Websocket Client Open Trigger is used for when any or a selected client opens.

For a detailed guide about the Websocket Client see [this page](/Servers-Clients/WebSocket-Clients).

## Configuration
### Client
Select any or a specific websocket client

## Variables
Name | Description
----:|:------------
`wsIdx` | The 0-based id of this websocket e.g. `0`, `1`, `2`, etc.
`wsId` | The UUID of this websocket client
`wsName` | The custom defined name of this websocket client
`wsUrl` | The full URL of this websocket client e.g. `ws://127.0.0.1:8080/`
`wsScheme` | The scheme of this websocket client e.g. `ws`
`wsHost` | The host of this websocket client e.g. `127.0.0.1`
`wsPort` | The port of this websocket client e.g. `8080`
`wsPath` | The path of this websocket client e.g.`/`
`wsQuery` | The query of this websocket client e.g.`?key=value`
`message` | {"timeStamp":"2023-03-16T22:58:28.3298+01:00","event":{"source":"HotKey","type":"Press"},"data":{"_85lbxopeOGvkNXq7iRgrjS6tpjj":1,"_hdhxue62iGbvG5rnMWU0dxGe29p":96}}

---

- [<i class="mdi mdi-chevron-left"></i>**Websocket Client Triggers Reference *Go Back***](/Triggers/Core/Websocket/Client)
- [<i class="mdi mdi-server-network primary--text"></i> **Open *Next Up***](/Triggers/Core/Websocket/Client/Open)
{.btn-grid .my-5}