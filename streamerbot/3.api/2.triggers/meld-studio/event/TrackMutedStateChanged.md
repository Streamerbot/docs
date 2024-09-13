---
title: TrackMutedStateChanged
description: Trigger for when the visibility of a layer changes in Meld Studio
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
    value: LayerVisibilityChanged
  - name: meldStudioEvent.trackId
    type: string
    description: The unique ID of the Track in Meld Studio
    value: 46DF14C0C929886EFDD7AC399EA754AF
  - name: meldStudioEvent.trackName
    type: string
    description: The name of the Track in Meld Studio
    value: Game Track
  - name: meldStudioEvent.muted
    type: bool
    description: Whether or not the Track is muted in Meld Studio
    value: False
  - name: meldStudioEvent._json
    type: json
    description: The full JSON payload from the event in Meld Studio
    value: {"trackId":"46DF14C0C929886EFDD7AC399EA754AF","trackName":"Game Track","muted":false}
---

## Parameters
::field-group
  ::field{name=Connection type=Select required}
    Choose a configured Meld Connection
    - Select `Any` to trigger on any connection
  ::
  ::field{name=Event type=Select required}
    Choose the name of the event to set the Trigger
    - Select `TrackMutedStateChanged` for this event
  ::
::
