::code-group
  ```csharp [Method]
  int TtsSpeak(string voiceAlias, string message, bool badWordFilter = false);
  ```
  ```csharp [Example]
  CPH.TtsSpeak("default", "Hello, world!", true);
  ```
::