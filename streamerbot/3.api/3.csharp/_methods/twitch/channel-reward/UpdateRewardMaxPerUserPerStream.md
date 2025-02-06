---
description: Updates the total maximum amount of redemptions per stream, per user, for the specified reward
version: 0.2.4
parameters:
  - import: TwitchRewardId
  - name: redeems
    type: number
    description: Amount of maximum redemptions per stream
    default: 1
  - name: additive
    type: boolean
    description: |
      - `true`  - Will add the value of `redeems` parameter to the current amount of max redeems per user
      - `false` - Will set the current amount of max redeems per user to the value of `redeems` parameter
    default: false
---
