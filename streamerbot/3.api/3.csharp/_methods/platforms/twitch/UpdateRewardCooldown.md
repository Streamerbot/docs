::code-group
  ```csharp [Method]
  void UpdateRewardCooldown(string rewardId, int cooldown, bool additive = null);
  ```
  ```csharp [Example]
  // Adds 10s to current cooldown
  CPH.UpdateRewardCooldown("a2d00d8c-89ef-4f59-aac5-0030a01a53f6", 10, true);

  // Sets cooldown to 10s
  CPH.UpdateRewardCooldown("a2d00d8c-89ef-4f59-aac5-0030a01a53f6", 10);
  ```
::