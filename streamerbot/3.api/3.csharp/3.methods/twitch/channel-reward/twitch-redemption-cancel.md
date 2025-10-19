---
name: TwitchRedemptionCancel
title: TwitchRedemptionCancel
description: Will refund the Twitch reward and removing it from the reward queue
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
            //Get redemption id
            CPH.TryGetArg("redemptionId",out string redemptionId);

            //Cancel Reward Redeem can get bool that indicates if successful
            bool refundSuccess = CPH.TwitchRedemptionCancel(rewardId, redemptionId);
            return true;
        }
    }
---
