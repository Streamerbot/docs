---
title: Version 0.0.57
description: 
published: true
date: 2023-06-11T15:02:32.898Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:36:32.509Z
---

* Misc fixes/updates
* Fixes for StreamElements, some typo's got past me
* Channel Rewards were loaded even if user was not an affiliate or partner, causing a crash
* Fix sub-action groupings not being loaded in the proper order, check any you may have setup, they may appear different
* Fix actions not properly propagating return state
* Fix deserialization of channel info, its possible for a user's game id to be null (yay?)
{.changelog-fixes}

<span></span>

* Delays are now there own Sub-action instead of the before/after
* Audio playback is handled as actions happen now, and will only block if in a blocking queue
* Weights can now be applied to sub-actions when the `Action` is set to `Random`, or the `Group` is set to `Random`
* Only one instance of Streamer.bot can be run
{.changelog-new}

## New Delay Sub-Action
Delays are now sub-actions that you can place anywhere, and are no longer tied to another sub-action.

On first load from previous versions, it will attempt to do a conversion from old delay style to new.  This is a best effort, and while I've tried to make it work as best as it can, there maybe cases I have missed.  Double check your delays after this update!

## Audio Playback Changes
With audio playback changing.  Before, it use to have its own internal queue that would handle all audio playback, and give you the option to play immediately.  Now, audio plays as the action happens, and it can also wait for the audio to finish before continuing on with any further actions.

THe option to play immediately has been replaced with finish before continuing, and defaults to true for first load of the sub-actions, and the creation of any new sub-action.

To have the old behaviour, any actions that contain a play audio or play audio from folder sub-action should be placed in a blocking queue, so they will wait appropriately.

## Weighted Values
You now have the capability to apply weights to sub-actions (and groups if the primary action is set to random).

For the moment, you will apply a weight as a decimal value (`0.5`), weights are a bit different then a raw percentage, altho, it can be treated as such if you don't want it to get move involved in the calculations.

Say you have 4 items, and you want them to be weighted equally for randomness, you can either enter a value of `1`, or `0.25` for each weight, and the underlying code will handle the normalization of this into percentage chances.

If the weight is left at 0, a random value will be assigned for the weight.

The working weighted list of actions will be cached first run through, and will be invalidated any time the weight of a sub-action or group is changed, or if a sub-action/group is added or deleted.

Before if you wanted something to have a higher chance of running, the work around was to house it in a separate action and put this in your primary action multiple times, this is no longer needed.

I can give a more technical breakdown of how it works for those that would like to know the inner details.