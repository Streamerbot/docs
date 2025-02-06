---
description: Get a list of all Twitch users with a given variable, along with their values
parameters:
  - import: GlobalVarName
  - import: GlobalPersisted
example: |
  using System;
  using System.Collections.Generic; //Needed cause of List<> usage

  public class CPHInline
  {
      public bool Execute()
      {
          //Get the user var list which is a List of type UserVariableValue with a specific type 
          List<UserVariableValue<long>> userVarList = CPH.GetTwitchUsersVar<long>("userVar", true);
          
          //For each loop which prints infos into Log File of the userVarList
          foreach(UserVariableValue<long> userVar in userVarList)
          {
              string displayName = userVar.UserName;
              string userId = userVar.UserId;
              string userLogin = userVar.UserLogin;
              
              //Actual value of user variable must be of same type previousy defined 
              long value = userVar.Value;
              
              //Last time the user var was updated for the user
              DateTime lastUpdate = userVar.LastWrite;
              
              CPH.LogInfo($"{displayName} - {userId} - {userLogin} - {value} - {lastUpdate}");
          }
          return true;
      }
  }
---