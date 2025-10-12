---
title: EventSource
description: C# enum definition for EventSource
name: EventSource
---

Within any action, the value of the `eventSource` variable can be retrieved using the `CPH.GetSource()` method, which returns an `EventSource` enum value.

This enum represents the source of the event that triggered the action.

## Usage Example

:read-more{to=/api/csharp/methods/core/events/get-source}

```csharp
using System;

public class CPHInline
{
  public bool Execute()
  {
    // Get the EventSource for the current action
    EventSource source = CPH.GetSource();

    // Compare EventSource with switch or if
    switch(source)
    {
      case EventSource.Twitch:
        // Do something with Twitch events...
        break;
      case EventSource.YouTube:
        // Do something with YouTube events...
        break;
    }

    return true;
  }
}
```

## Enum Values

| Value                             | Description                                    |
| --------------------------------- | ---------------------------------------------- |
| EventSource.Application           | [No description provied]{.text-muted .text-xs} |
| EventSource.Command               | [No description provied]{.text-muted .text-xs} |
| EventSource.CrowdControl          | [No description provied]{.text-muted .text-xs} |
| EventSource.Custom                | [No description provied]{.text-muted .text-xs} |
| EventSource.DonorDrive            | [No description provied]{.text-muted .text-xs} |
| EventSource.Elgato                | [No description provied]{.text-muted .text-xs} |
| EventSource.FileTail              | [No description provied]{.text-muted .text-xs} |
| EventSource.FileWatcher           | [No description provied]{.text-muted .text-xs} |
| EventSource.Fourthwall            | [No description provied]{.text-muted .text-xs} |
| EventSource.General               | [No description provied]{.text-muted .text-xs} |
| EventSource.Group                 | [No description provied]{.text-muted .text-xs} |
| EventSource.HypeRate              | [No description provied]{.text-muted .text-xs} |
| EventSource.Inputs                | [No description provied]{.text-muted .text-xs} |
| EventSource.Invalid               | [No description provied]{.text-muted .text-xs} |
| EventSource.Kick                  | [No description provied]{.text-muted .text-xs} |
| EventSource.Kofi                  | [No description provied]{.text-muted .text-xs} |
| EventSource.MeldStudio            | [No description provied]{.text-muted .text-xs} |
| EventSource.Midi                  | [No description provied]{.text-muted .text-xs} |
| EventSource.Misc                  | [No description provied]{.text-muted .text-xs} |
| EventSource.Obs                   | [No description provied]{.text-muted .text-xs} |
| EventSource.Pallygg               | [No description provied]{.text-muted .text-xs} |
| EventSource.Patreon               | [No description provied]{.text-muted .text-xs} |
| EventSource.Pulsoid               | [No description provied]{.text-muted .text-xs} |
| EventSource.Quote                 | [No description provied]{.text-muted .text-xs} |
| EventSource.Raw                   | [No description provied]{.text-muted .text-xs} |
| EventSource.Shopify               | [No description provied]{.text-muted .text-xs} |
| EventSource.SpeakerBot            | [No description provied]{.text-muted .text-xs} |
| EventSource.SpeechToText          | [No description provied]{.text-muted .text-xs} |
| EventSource.StreamDeck            | [No description provied]{.text-muted .text-xs} |
| EventSource.StreamElements        | [No description provied]{.text-muted .text-xs} |
| EventSource.StreamerBot           | [No description provied]{.text-muted .text-xs} |
| EventSource.StreamerBotRemote     | [No description provied]{.text-muted .text-xs} |
| EventSource.Streamlabs            | [No description provied]{.text-muted .text-xs} |
| EventSource.StreamlabsDesktop     | [No description provied]{.text-muted .text-xs} |
| EventSource.System                | [No description provied]{.text-muted .text-xs} |
| EventSource.ThrowingSystem        | [No description provied]{.text-muted .text-xs} |
| EventSource.TipeeeStream          | [No description provied]{.text-muted .text-xs} |
| EventSource.TreatStream           | [No description provied]{.text-muted .text-xs} |
| EventSource.Trovo                 | [No description provied]{.text-muted .text-xs} |
| EventSource.Twitch                | [No description provied]{.text-muted .text-xs} |
| EventSource.VoiceMod              | [No description provied]{.text-muted .text-xs} |
| EventSource.VTubeStudio           | [No description provied]{.text-muted .text-xs} |
| EventSource.WebsocketClient       | [No description provied]{.text-muted .text-xs} |
| EventSource.WebsocketCustomServer | [No description provied]{.text-muted .text-xs} |
| EventSource.YouTube               | [No description provied]{.text-muted .text-xs} |
