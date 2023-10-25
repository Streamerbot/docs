::code-group
  ```csharp [Method]
  string ObsSendRaw(string requestType, string data, int connection = 0);
  ```
  ```csharp [Example]
  string result = CPH.ObsSendRaw("GetSourceActive", "{\"sourceName\":\"Camera\"}");
  ```
::