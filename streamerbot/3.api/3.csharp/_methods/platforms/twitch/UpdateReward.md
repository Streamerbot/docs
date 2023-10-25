::code-group
  ```csharp [Method]
  bool UpdateReward(string rewardId, string title = null, string prompt = null, int? cost = null, string backroundColor = null);
  ```
  ```csharp [Example]
  CPH.UpdateReward("a2d00d8c-89ef-4f59-aac5-0030a01a53f6", "My Reward", "A reward description", 200, "#FF0000");
  ```
::