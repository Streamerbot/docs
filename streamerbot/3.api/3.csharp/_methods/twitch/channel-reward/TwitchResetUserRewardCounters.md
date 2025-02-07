---
description: Reset all user reward counters for the specified user, by id
parameters:
  - import: TwitchRewardId
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get user id of current user id
            CPH.TryGetArg("userId",out string userId);
            
            //Reset persisted user reward counter 
            CPH.TwitchResetUserRewardCounters(userId, true);
            return true;
        }
    }
---