---
description: Get the amount of channel points used by a user. Tracks only the redeems that Streamer.bot has seen.
parameters:
  - name: userId
    type: string
    description: Twitch Id of the user
    default: '"1234567"'
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get user id of current user
            CPH.TryGetArg("userId",out string userId);
            //Get amount
            long amount = CPH.TwitchGetChannelPointsUsedByUserId(userId);
            //Set as argument example
            CPH.SetArgument("amountSpend",amount);
            return true;
        }
    }
---