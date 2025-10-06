---
name: TwitchGetRewardUserCounter
title: TwitchGetRewardUserCounter
description: Returns reward count of the given reward for a specified Twitch user
version: 0.2.4
parameters:
  - import: TwitchRewardId
  - import: UserName
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define reward id of reward you want counter
            string rewardId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            //Get user login
            CPH.TryGetArg("userName",out string userLogin);
            //Get persisted reward counter info of for specific user
            TwitchRewardCounter rewardCounter = CPH.TwitchGetRewardUserCounter(userLogin, rewardId, true);
            //Get counter
            int counter = rewardCounter.Count;
            //Set Argumnet for counter
            CPH.SetArgument("rewardUserCounter", counter);
            return true;
        }
    }
---
