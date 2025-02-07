---
description: Mark Twitch reward as resolved, which makes the redeem non refundable and removes it from reward queue
parameters:
  - import: TwitchRewardId
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
            
            //Fulfill Reward Redeem can get bool that indicates if successful
            bool refundSuccess = CPH.TwitchRedemptionFulfill(rewardId, redemptionId);
            return true;
        }
    }
---
