---
version: 0.0.30
---

# Reward Redemption
When someone redeems a reward redemption

## Details
::list
- Twitch Service: `PubSub`
::

## Variables
:variables-description

Name | Description
----:|:------------
`redemptionId` | String identifier for this redemption (used to refund reward) <br> `4d9f236b-7486-481a-89af-1d03676d5275`
`rewardId` | String identifier for this reward <br> `44e86f71-8ace-4739-a123-3ff095489343`
`rewardName` | Name of the reward <br> `My Reward`
`rewardPrompt` | The verbiage shown on the channel point description <br> `My cool Reward Prompt`
`rewardCost` | The channel point cost of the redeemed reward  <br> `100`
`counter` | Number of times this reward has been redeemed <br> `1`
`userCounter` | Number of times the same user has redeemed this reward <br> `1`
`rawInput` | String text entered by the user (if required) <br> `https://streamer.bot/Test Unescaped Text $$$`
`rawInputEscaped` | String text entered by the user (escaped) <br> `https://streamer\.bot/Test Escaped Text \$\$\$`

:variables{name=TwitchUser disclosure}