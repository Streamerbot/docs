---
description: Fetch a global variable by name
parameters:
  - import: GlobalVarName
  - import: GlobalPersisted
example: |
  int myInt = CPH.GetGlobalVar<int>("myInt");
  int myString = CPH.GetGlobalVar<string>("myString");
---