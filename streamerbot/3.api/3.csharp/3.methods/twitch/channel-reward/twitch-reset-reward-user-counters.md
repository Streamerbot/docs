---
name: TwitchResetRewardUserCounters
title: TwitchResetRewardUserCounters
description: Reset reward user counters for the specified reward, by id
parameters:
  - import: TwitchRewardId
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define reward id you want to reset counter of
            string rewardId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            CPH.TwitchResetRewardUserCounters(rewardId);
            return true;
        }
    }
---