---
name: TwitchResetUserRewardCounters
title: TwitchResetUserRewardCounters
description: Reset all user reward counters for the specified user, by id
parameters:
  - name: rewardId
    import: twitch/rewards/id
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