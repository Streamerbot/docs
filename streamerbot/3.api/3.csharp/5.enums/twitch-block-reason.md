---
title: TwitchBlockReason
description: C# enum definition for TwitchBlockReason
name: TwitchBlockReason
---

## Namespace

`Streamer.bot.Plugin.Interface.Enums`

## Definition

```cs [TwitchBlockReason.cs]
public enum TwitchBlockReason
{
    None,
    Harassment,
    Spam,
    Other
}
```

## Values

| Name                           | Description                             |
| ------------------------------ | --------------------------------------- |
| `TwitchBlockReason.None`       | No specific reason                      |
| `TwitchBlockReason.Harassment` | The user was blocked for harassment     |
| `TwitchBlockReason.Spam`       | The user was blocked for spamming       |
| `TwitchBlockReason.Other`      | The user was blocked for another reason |
