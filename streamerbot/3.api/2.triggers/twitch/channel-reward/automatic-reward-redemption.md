---
title: Automatic Reward Redemption
description: Trigger for when default channel point rewards or Power-ups have been used
version: 0.2.4
variables:
  - name: rewardType
    type: string
    description: type of the reward
    value: send_highlighted_message, random_sub_emote_unlock, chosen_sub_emote_unlock, chosen_modified_sub_emote_unlock, single_message_bypass_sub_mode, message_effect, gigantify_an_emote, celebration
  - name: rewardCost
    type: int
    description: cost of the reward
    value: 80
  - name: unlockedEmoteId
    type: string
    description: ID of the unlocked emote (obviously not available for all reward types)
    value: emotesv2_f5d843cf38bf42208d022e89a9de258e
  - name: unlockedEmoteName
    type: string
    description: name of the unlocked emote (obviously not available for all reward types)
    value: tawmaeKEKW
commonVariables:
  - TwitchUser
---

## Details
The Automatic Reward Redemption work for both "default rewards" and the newly introduced "Power-ups".

### Default Rewards
The default rewards are those made by Twitch like "Highlight My Message". You can either choose to enable or disable them, but you cannot delete or edit them.

![Default Rewards](../assets/default_rewards.png)

### Power Ups
Power-ups have been added on June 12, 2024 and are available in your Channel Reward window. It allows viewers to do specific interactions with bits.

![Default Rewards](../assets/power_ups.png)


In order to to filter for Power-ups in Streamer.bot, you can create an `if/else` subaction and check for the variable `rewardType`:

```
message_effect
gigantify_an_emote
celebration
```
