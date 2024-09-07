---
description: Returns a list of Twitch Reward
example: |
    using System;
    using System.Collections.Generic; //needed due to List usage
    public class CPHInline
    {
        public bool Execute()
        {
            //Get list of rewards
            List<TwitchReward> rewardList = CPH.TwitchGetRewards();
            
            //Example to go through list and write them to logfile
            foreach(TwitchReward reward in rewardList)
            {
                //Get id of current reward
                string id = reward.Id;
                //Get title of reward
                string title = reward.Title;
                //Get cost of current reward
                int cost = reward.Cost;

                //Write to log
                CPH.LogInfo($"RewardId:{id}, Reward Title: {title}, Cost: {cost}");
            }
            return true;
        }
    }
---
