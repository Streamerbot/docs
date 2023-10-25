::code-group
  ```csharp [Method]
  void PlaySoundFromFolder(string path, float volume = 1.0f, bool recursive = false, bool finishBeforeContinuing = false);
  ```
  ```csharp [Example]
  // Recursively play any sound file from the `Hall & Oates` directory
  CPH.PlaySoundFromFolder("C://Users/JohnDoe/Music/Hall & Oates", 1.0f, true);
  ```
::