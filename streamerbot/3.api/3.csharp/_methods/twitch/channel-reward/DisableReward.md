---
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
