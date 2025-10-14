---
title: TwitchBlockContext
description: C# enum definition for TwitchBlockContext
name: TwitchBlockContext
---

## Namespace

`Streamer.bot.Plugin.Interface.Enums`

## Definition

```cs [TwitchBlockContext.cs]
public enum TwitchBlockContext
{
    None,
    Chat,
    Whisper
}
```

## Values

| Name                         | Description                                  |
| ---------------------------- | -------------------------------------------- |
| `TwitchBlockContext.None`    | No specific context                          |
| `TwitchBlockContext.Chat`    | The block was initiated in a chat context    |
| `TwitchBlockContext.Whisper` | The block was initiated in a whisper context |
