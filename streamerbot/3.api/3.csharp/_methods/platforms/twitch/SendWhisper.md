::code-group
  ```csharp [Method]
  bool SendWhisper(string userName, string message, bool bot = true);
  ```
  ```csharp [Example]
  bool whisperSucces = SendWhisper("TwitchUser", "Whisper from bot account", true);
  ```
::