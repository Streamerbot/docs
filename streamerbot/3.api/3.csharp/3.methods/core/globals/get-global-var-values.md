---
name: GetGlobalVarValues
title: GetGlobalVarValues
description: Fetch a list of all global variable values
parameters:
  - import: GlobalPersisted
example: |
    using System;
    using System.Collections.Generic;//due to List usage
    public class CPHInline
    {
      public bool Execute()
      {
        //Get list of global variable values
        List<GlobalVariableValue> globalVarList = CPH.GetGlobalVarValues();
        
        //Example writing variable names into logs
        foreach(GlobalVariableValue globalVar in globalVarList)
        {
          //Get name of current globalVar
          string varName = globalVar.VariableName;
          //Get last write DateTime of current globalVar
          DateTime lastWrite = globalVar.LastWrite;
          
          CPH.LogInfo($"GlobalVarName : {varName}, LastWrite: {lastWrite}");
        }
        return true;
      }
    }
---