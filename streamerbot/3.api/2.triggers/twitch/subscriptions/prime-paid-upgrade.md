---
title: Prime Paid Upgrade
description: Triggered when a user upgrades their Prime subscription to a Tier 1, 2, or 3
twitchService: EventSub
version: 0.2.5
variables:
  - name: systemMessage
    type: string
    description: The message Twitch will send into Chat on this specific event
    version: 0.2.5
  - name: upgradeTier
    type: number
    description: The tier that the subscription was upgraded to
    value: 1000
  - name: upgradeTierString
    type: string
    description: The tier, in text form, that the subscription was upgraded to
    value: tier 1
commonVariables:
  - TwitchBroadcaster
  - TwitchUser
---
