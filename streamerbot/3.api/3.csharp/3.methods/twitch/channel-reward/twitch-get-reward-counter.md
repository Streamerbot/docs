---
name: TwitchGetRewardCounter
title: TwitchGetRewardCounter
description: Get the counter of a Twitch reward, by id
parameters:
  - import: TwitchRewardId
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define reward id of reward you want counter
            string rewardId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";

            //Get persisted reward counter info
            TwitchRewardCounter rewardCounter = CPH.TwitchGetRewardCounter(rewardId, true);
            //Get counter
            int counter = rewardCounter.Count;
            //Set Argumnet for counter
            CPH.SetArgument("rewardCounter", counter);
            return true;
        }
    }
---