::list{type=warning}
- Must import `Streamer.bot.Common.Events`
::

::code-group
  ```csharp [Method]
  EventType GetEventType();
  ```
  ```csharp [Example]
  using System;
  using Streamer.bot.Common.Events; // REQUIRED

  public class CPHInline
  {
    public bool Execute()
    {
      // Get the current event type
      EventType eventType = CPH.GetEventType();

      // Check if the current event type is YouTubeFirstWords
      bool isFirstWords = eventType == EventType.YouTubeFirstWords;

      return true;
    }
  }

  ```
::