---
name: GetEventType
title: GetEventType
description: Fetch the value of the `__source` variable
example: |
  using System;

  public class CPHInline
  {
    public bool Execute()
    {
      // Get the EventType for the current action
      EventType eventType = CPH.GetEventType();

      // Compare EventType with switch or if
      switch(eventType)
      {
        case EventType.TwitchSub:
          // Do something with TwitchSub events...
          break;
        case EventType.TwitchReSub:
          // Do something with TwithReSub events...
          break;
      }

      return true;
    }
  }
---