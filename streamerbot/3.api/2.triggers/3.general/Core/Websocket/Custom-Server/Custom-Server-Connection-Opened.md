---
title: Custom Server Connection Opened
description: Websocket Custom Server Reference
published: true
date: 2023-04-18T00:23:22.662Z
tags: 
editor: markdown
dateCreated: 2023-04-18T00:15:36.923Z
---

## Overview
This triggers when a client connects to the custom websocket server.

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

---

- [<i class="mdi mdi-chevron-left"></i>**Websocket Custom Server Triggers Reference *Go Back***](/Triggers/Core/Websocket/Custom-Server)
- [<i class="mdi mdi-message-text primary--text"></i> **Custom Server Message *Up Next***](/Triggers/Core/Websocket/Custom-Server/Custom-Server-Message)
{.btn-grid .my-5}