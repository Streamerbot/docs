---
title: Ad Mid-Roll
description: Trigger for a Twitch Ad Mid-Roll
version: 0.1.15
twitchService: PubSub
variables:
  - name: ad.commercialId
    type: string
    description: The ID of the ad that's about to run
  - name: ad.jitterTime
    type: number
    description: How long until the ad runs in milliseconds
  - name: ad.warmupTime
    type: number
    description: How long until the ad runs in milliseconds
---

::warning
It is **not recommended** to rely on this trigger.
- This trigger utilizes an **undocumented and unsupported** Twitch PubSub event which could be removed, without warning, in the future.
::

## Details
This event triggers 5 seconds prior to the start of an ad.

See the [Ad Run](/api/triggers/twitch/ads/ad-run) trigger if you are looking for the ad start event.