---
title: Ad Run
description: Trigger for a Twitch Ad Run
version: 0.1.10
twitchService: EventSub
variables:
  - name: adLength
    type: number
    description: The length of the ad in seconds
    value: 90
  - name: adLengthMs
    type: number
    description: The length of the ad in milliseconds
    value: 90000
  - name: adScheduled
    type: boolean
    description: Is the ad scheduled?
    value: true
commonVariables:
  - TwitchBroadcaster
---

This event triggers at the start of an ad break.