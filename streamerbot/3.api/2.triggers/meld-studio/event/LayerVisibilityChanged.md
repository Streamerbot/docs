---
title: LayerVisibilityChanged
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
  - name: meldStudioEvent.layerId
    type: string
    description: The unique ID of the layer in Meld Studio
    value: D51F56E984CE10AD7E90C09F68E60710
  - name: meldStudioEvent.layerName
    type: string
    description: The name of the layer in Meld Studio
    value: Text 3
  - name: meldStudioEvent.visible
    type: bool
    description: Whether or not the layer is visible in Meld Studio
    value: True
  - name: meldStudioEvent._json
    type: string
    description: Full JSON Payload of the event in Meld Studio
    value: {"layerId":"D51F56E984CE10AD7E90C09F68E60710","layerName":"Text 3","visible":true} 
---

## Parameters
::field-group
  ::field{name=Connection type=Select required}
    Choose a configured Meld Connection
    - Select `Any` to trigger on any connection
  ::
  ::field{name=Event type=Select required}
    Choose the name of the event to set the Trigger
    - Select `LayerVisibilityChanged` for this event
  ::
::
