---
version: 0.1.15
---

# Ad Mid-Roll
Twitch mid-roll ad trigger.

## Details
::list
- Twitch Service: `PubSub`
::

This event triggers 5 seconds prior to the start of an ad.

See the [Ad Run](/api/triggers/platforms/twitch/ads/ad-run) trigger if you are looking for the ad start event.

## Variables
:variables-description

Name | Description
----:|:------------
`ad.commercialId` | The ID of the ad that's about to run.
`ad.jitterTime` | How long until the ad runs in milliseconds.
`ad.warmupTime` | How long until the ad runs in milliseconds.