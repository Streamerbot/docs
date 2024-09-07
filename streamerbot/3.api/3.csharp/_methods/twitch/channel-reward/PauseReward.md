---
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define reward id you want to pause
            string rewardId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            
            CPH.PauseReward(rewardId);
            return true;
        }
    }
---