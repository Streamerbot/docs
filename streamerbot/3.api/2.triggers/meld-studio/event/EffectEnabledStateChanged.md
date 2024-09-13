---
title: EffectEnabledStateChange
description: Trigger for when the Enabled State of an Effect occurs in Meld Studio
version: 0.2.5
variables:
  - name: meldStudio.id
    type: string
    description: The connection id
    value: 0a92da3b-be05-4780-a960-26eac5788f79
  - name: meldStudio.name
    type: string
    description: The name of the connection
    value: Meld Studio Main
  - name: meldStudio.host
    type: string
    description: The IP Address of the Meld Studio connection
    value: 127.0.0.1
  - name: meldStudioEvent.event
    type: string
    description: The name of the event that occurred in Meld Studio
    value: TrackMonitoringStateChanged
  - name: meldStudioEvent.effectId
    type: string
    description: The unique ID of the effect in Meld Studio
    value: 155890E6AA46DF9B2A56D8BF0F891322
  - name: meldStudioEvent.effectName
    type: string
    description: The name of the effect in Meld Studio
    value: Black and White
  - name: meldStudioEvent.enabled
    type: boolean
    description: Whether the effect in Meld Studio is enabled or not
    value: True
  - name: meldStudioEvent._json
    type: string
    description: The full JSON payload of the effect in Meld Studio
    value: {"effectId":"155890E6AA46DF9B2A56D8BF0F891322","effectName":"Black and White","enabled":true}
---

## Parameters
::field-group
  ::field{name=Connection type=Select required}
    Choose a configured Meld Connection
    - Select `Any` to trigger on any connection
  ::
  ::field{name=Event type=Select required}
    Choose the name of the event to set the Trigger
    - Select `EffectEnabledStateChanged` for this event
  ::
::
