---
title: ObjectUpdated
description: Trigger for when any Object is updated in Meld Studio
version: 0.2.5
parameters:
  - name: MeldStudioConnection
  - name: Event
    type: Select
    required: true
    description: |
      Choose the name of the event to set the Trigger
      - Select `ObjectUpdated` for this event
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
    value: ObjectUpdated
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
    value: True
  - name: meldStudioEvent.object.id
    type: string
    description: The unique ID of the object in Meld Studio
    value: EC495E605169EF94FE380E10A57EBF82
  - name: meldStudioEvent.object.name
    type: string
    description: The name of the object in Meld Studio
    value: Image 20
  - name: meldStudioEvent._json
    type: string
    description: The full JSON payload of the effect in Meld Studio
    value: {"id":"EC495E605169EF94FE380E10A57EBF82","name":"Image 20","objectType":"layer","object":{"index":2,"parent":"B628E10FA3EBEE0BC0F1C785CA1C808E","visible":true,"id":"EC495E605169EF94FE380E10A57EBF82","name":"Image 20"}}
---
