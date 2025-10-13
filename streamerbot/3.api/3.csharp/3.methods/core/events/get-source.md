---
name: GetSource
title: GetSource
description: Fetch the value of the `eventSource` variable
example: |
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
---