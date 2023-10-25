---
title: Custom Server Message
description: Websocket Custom Server Reference
published: true
date: 2023-04-18T00:22:45.464Z
tags: 
editor: markdown
dateCreated: 2023-04-18T00:22:43.500Z
---

## Overview
This triggers when a client sends a message the custom websocket server.

For a detailed guide about Websocket Servers see [this page](/Servers-Clients/WebSocket-Servers).

## Configuration
### Server
Select any or a specific websocket server

## Variables
Name | Description
----:|:------------
`wssIdx` | The 0-based id of this websocket server e.g. `0`, `1`, `2`, etc.
`wssId` | The UUID of this websocket server
`ip` | The ip of this websocket serber e.g. `127.0.0.1`
`sessionId` | The session id of the client
`data` | The received data from the client

---

- [<i class="mdi mdi-chevron-left"></i>**Websocket Custom Server Triggers Reference *Go Back***](/Triggers/Core/Websocket/Custom-Server)
- [<i class="mdi mdi-server-network-off primary--text"></i> **Custom Server Connection Closed *Up Next***](/Triggers/Core/Websocket/Custom-Server/Custom-Server-Connection-Closed)
{.btn-grid .my-5}