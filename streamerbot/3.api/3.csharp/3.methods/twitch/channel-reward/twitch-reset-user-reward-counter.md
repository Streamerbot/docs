---
name: TwitchResetUserRewardCounter
title: TwitchResetUserRewardCounter
description: Reset user reward counters for the specified reward id and user Id
parameters:
  - import: TwitchRewardId
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define reward id you want to reset user counter of
            string rewardId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            //Get user id of current user id
            CPH.TryGetArg("userId",out string userId);
            
            CPH.TwitchResetUserRewardCounter(rewardId, userId);
            return true;
        }
    }
---