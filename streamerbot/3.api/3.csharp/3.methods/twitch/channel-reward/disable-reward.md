---
name: DisableReward
title: DisableReward
description: Disable a Twitch Channel Point Reward, owned by Streamer.bot
parameters:
  - name: rewardId
    import: twitch/rewards/id
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get current rewardId
            CPH.TryGetArg("rewardId",out string rewardId);

            //Disable Reward
            CPH.DisableReward(rewardId);
            return true;
        }
    }
---
