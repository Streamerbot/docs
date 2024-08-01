---
description: Fetch a global variable by name
parameters:
  - import: GlobalVarName
  - import: GlobalPersisted
example: |
  int myInt = CPH.GetGlobalVar<int>("myInt");
  string myString = CPH.GetGlobalVar<string>("myString");
---
