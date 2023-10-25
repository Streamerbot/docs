# Get Reward Info
Get the info from a reward.
:image-preview

## Parameters
### `Reward`
Choose the reward where you want to get the info from.

## Variables
:variables-description
Name | Description
----:|:------------
`rewardId` | String identifier for this reward
`rewardTitle` | The title of the reward
`rewardBackgroundColor` | The background color of the reward
`rewardEnabled` | If the reward is enabled
`rewardPrompt` | The verbiage shown on the channel point description
`rewardSkipReuqestQueue` | If there is a skip request in the queue
`rewardCost` | The cost of the reward

## C# Usage
:csharp-method{name=TwitchGetRewards}