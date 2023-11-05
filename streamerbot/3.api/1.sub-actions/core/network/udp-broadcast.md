---
title: UDP Broadcast
description: Network Sub-Actions Reference
published: true
date: 2023-04-10T05:36:14.717Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:34:25.751Z
---

## Overview
Broadcast a UDP payload on a specified port

![image](/119697611-46d1a800-be48-11eb-8e09-696fe4060a58.png =400x)

## Example: Send text to Speaker.bot to be read out

```json
{
  "command": "speak",
  "id": "1234",
  "voice": "BotVoice",
  "message": "It's %user%"
}
```

Replace `BotVoice` with the alias you want Speaker.bot to use, and `message` with the text you would like spoken

---

- [<i class="mdi mdi-chevron-left"></i>**Network Sub-Actions Reference *Go Back***](/Sub-Actions/Network)
{.btn-grid .my-5}