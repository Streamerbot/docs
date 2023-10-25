::code-group
  ```csharp [Method]
  T GetGlobalVar<T>(string varName, bool persisted = true);
  ```
  ```csharp [Example]
  string myVariable = CPH.GetGlobalVar<string>("myVariable");
  ```
::