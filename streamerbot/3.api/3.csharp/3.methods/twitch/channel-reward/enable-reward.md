---
name: EnableReward
title: EnableReward
description: Enable a Twitch Channel Point Reward, owned by Streamer.bot
parameters:
  - name: rewardId
    import: twitch/rewards/id
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define reward id you want to enable
            string rewardId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";

            CPH.EnableReward(rewardId);
            return true;
        }
    }
---
