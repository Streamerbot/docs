---
title: Ad Run
description: Trigger for a Twitch Ad Run
version: 0.1.10
twitchService: PubSub
variables:
  - name: adLength
    type: number
    description: The length of the ad in seconds
    value: 90
  - name: adScheduled
    type: boolean
    description: Is the ad scheduled?
    value: true
---

## Details
This event triggers at the start of an ad.

See the [Ad Mid-Roll](/api/triggers/twitch/ads/ad-mid-roll) trigger if you are looking for an 5 seconds prior to the ad event.