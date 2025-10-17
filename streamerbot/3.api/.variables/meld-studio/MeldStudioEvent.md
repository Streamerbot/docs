---
title: Meld Studio Event Variables
navigation.title: Meld Studio Event
variables:
  - name: meldStudio.id
    type: string
    description: ID of the connection this event originated from
    value: 0a92da3b-be05-4780-a960-26eac5788f79
  - name: meldStudio.name
    type: string
    description: Name of the connection this event originated from
    value: Meld Studio Main
  - name: meldStudio.host
    type: string
    description: IP Address of the connection this event originated from
    value: 127.0.0.1
  - name: meldStudioEvent._json
    type: string
    description: Raw JSON payload of the event from Meld Studio
    value: '{"effectId":"155890E6AA46DF9B2A56D8BF0F891322","effectName":"Black and White","enabled":true}'
  - name: meldStudioEvent.event
    type: string
    description: Name of the event that occurred in Meld Studio
    value: TrackMonitoringStateChanged
    filter:
      - value: EffectEnabledStateChanged
        children:
          - name: meldStudioEvent.event
            value: EffectEnabledStateChanged
          - name: meldStudioEvent._json
            value: '{"effectId":"155890E6AA46DF9B2A56D8BF0F891322","effectName":"Black and White","enabled":true}'
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
            value: true
      - value: LayerVisibilityChanged
        children:
          - name: meldStudioEvent.event
            value: LayerVisibilityChanged
          - name: meldStudioEvent._json
            value: '{"layerId":"D51F56E984CE10AD7E90C09F68E60710","layerName":"Text 3","visible":true}'
          - name: meldStudioEvent.layerId
            type: string
            description: The unique ID of the layer in Meld Studio
            value: D51F56E984CE10AD7E90C09F68E60710
          - name: meldStudioEvent.layerName
            type: string
            description: The name of the layer in Meld Studio
            value: Text 3
          - name: meldStudioEvent.visible
            type: boolean
            description: Whether or not the layer is visible in Meld Studio
            value: true
      - value: ObjectAdded
        children:
          - name: meldStudioEvent.event
            value: ObjectAdded
          - name: meldStudioEvent._json
            value: '{"id":"EC495E605169EF94FE380E10A57EBF82","name":"Image 1","objectType":"layer","object":{"index":1,"parent":"B628E10FA3EBEE0BC0F1C785CA1C808E","visible":true,"id":"EC495E605169EF94FE380E10A57EBF82","name":"Image 1"}}'
          - name: meldStudioEvent.id
            type: string
            description: The unique ID of the event that occurred in Meld Studio
            value: EC495E605169EF94FE380E10A57EBF82
          - name: meldStudioEvent.name
            type: string
            description: The name of the event that occured in Meld Studio
            value: Image 1
          - name: meldStudioEvent.objectType
            type: string
            description: The type of the object in Meld Studio
            value: layer
          - name: meldStudioEvent.object.index
            type: number
            description: The index number of the object in Meld Studio
            value: Image 1
          - name: meldStudioEvent.object.parent
            type: string
            description: The ID of the parent of the object in Meld Studio
            value: B628E10FA3EBEE0BC0F1C785CA1C808E
          - name: meldStudioEvent.object.visible
            type: boolean
            description: Whether the object is visible in Meld Studio
            value: true
          - name: meldStudioEvent.object.id
            type: string
            description: The unique ID of the object in Meld Studio
            value: EC495E605169EF94FE380E10A57EBF82
          - name: meldStudioEvent.object.name
            type: string
            description: The name of the object in Meld Studio
            value: Image 1
      - value: ObjectUpdated
        children:
          - name: meldStudioEvent.event
            value: ObjectUpdated
          - name: meldStudioEvent._json
            value: '{"id":"EC495E605169EF94FE380E10A57EBF82","name":"Image 20","objectType":"layer","object":{"index":2,"parent":"B628E10FA3EBEE0BC0F1C785CA1C808E","visible":true,"id":"EC495E605169EF94FE380E10A57EBF82","name":"Image 20"}}'
          - name: meldStudioEvent.id
            type: string
            description: The unique ID of the event that occurred in Meld Studio
            value: EC495E605169EF94FE380E10A57EBF82
          - name: meldStudioEvent.name
            type: string
            description: The name of the event that occured in Meld Studio
            value: Image 20
          - name: meldStudioEvent.objectType
            type: string
            description: The type of the object in Meld Studio
            value: layer
          - name: meldStudioEvent.object.index
            type: number
            description: The index number of the object in Meld Studio
            value: Image 2
          - name: meldStudioEvent.object.parent
            type: string
            description: The ID of the parent of the object in Meld Studio
            value: B628E10FA3EBEE0BC0F1C785CA1C808E
          - name: meldStudioEvent.object.visible
            type: boolean
            description: Whether the object is visible in Meld Studio
            value: true
          - name: meldStudioEvent.object.id
            type: string
            description: The unique ID of the object in Meld Studio
            value: EC495E605169EF94FE380E10A57EBF82
          - name: meldStudioEvent.object.name
            type: string
            description: The name of the object in Meld Studio
            value: Image 20
      - value: TrackMonitoringStateChanged
        children:
          - name: meldStudioEvent.event
            value: TrackMonitoringStateChanged
          - name: meldStudioEvent._json
            value: '{"trackId":"46DF14C0C929886EFDD7AC399EA754AF","trackName":"Game Track","monitoring":false}'
          - name: meldStudioEvent.trackId
            type: string
            description: The unique ID of the Track in Meld Studio
            value: 46DF14C0C929886EFDD7AC399EA754AF
          - name: meldStudioEvent.trackName
            type: string
            description: The name of the Track in Meld Studio
            value: Game Track
          - name: meldStudioEvent.monitoring
            type: boolean
            description: Whether or not the Track is monitored in Meld Studio
            value: false
      - value: TrackMutedStateChanged
        children:
          - name: meldStudioEvent.event
            value: TrackMutedStateChanged
          - name: meldStudioEvent._json
            value: '{"trackId":"46DF14C0C929886EFDD7AC399EA754AF","trackName":"Game Track","muted":false}'
          - name: meldStudioEvent.trackId
            type: string
            description: The unique ID of the Track in Meld Studio
            value: 46DF14C0C929886EFDD7AC399EA754AF
          - name: meldStudioEvent.trackName
            type: string
            description: The name of the Track in Meld Studio
            value: Game Track
          - name: meldStudioEvent.muted
            type: boolean
            description: Whether or not the Track is muted in Meld Studio
            value: false
---


