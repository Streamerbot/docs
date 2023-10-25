::list{type=warning}
- Must import `Streamer.bot.Common.Events`
::

::code-group
  ```csharp [Method]
  EventSource GetSource();
  ```
  ```csharp [Example]
  using System;
  using Streamer.bot.Common.Events; // REQUIRED

  public class CPHInline
  {
    public bool Execute()
    {
      // Get the current event source
      EventSource currentSource = CPH.GetSource();

      // Check if the current source is Twitch
      bool isTwitch = currentSource == EventSource.Twitch;

      return true;
    }
  }

  ```
::