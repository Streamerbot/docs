---
description: Returns a list of Twitch Reward Counters
parameters:
  - import: TwitchRewardId
  - name: persisted
    type: boolean
    default: true
    description: If true will use the persisted user counters of the reward, if not the non-persisted.
example: |
    using System;
    using System.Collections.Generic; //needed due to List usage
    public class CPHInline
    {
        public bool Execute()
        {
            //Reward Id of the channel point reward you want to get your counters of
            string rewardId = "your reward id";
            //Whether or not you want to get the persisted or non persisted counters
            bool persisted = true;

            List<TwitchRewardCounter> rewardCounters = CPH.TwitchGetRewardUserCounters(rewardId, true);

            foreach(TwitchRewardCounter userCounter in rewardCounters)
            {
                string displayName = userCounter.UserName;
                int counter = userCounter.Count;

                CPH.LogInfo($"{displayName} has Count of {counter}.");
            }
            return true;
        }
    }
---
