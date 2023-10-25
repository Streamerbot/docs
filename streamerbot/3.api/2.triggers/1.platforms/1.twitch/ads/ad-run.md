---
version: 0.1.10
---

# Ad Run
Twitch ad start trigger.

## Details
::list
- Twitch Service: `PubSub`
::

This event triggers at the start of an ad.

See the [Ad Mid Roll](/api/triggers/platforms/twitch/ads/ad-mid-roll) trigger if you are looking for an 5 seconds prior to the ad event.

## Variables
:variables-description

Name | Description
----:|:------------
`adLength` | The length of the ad in seconds.
`adScheduled` | If this ad was scheduled. Returns `True` or `False`.
