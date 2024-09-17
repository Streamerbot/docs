---
title: OBS Scene Changed
description: Trigger for when an OBS Scene is Changed
version: 0.2.0
parameters:
  - name: ObsConnection
    type: Select
    required: true
    description: |
      Select the Connection from the drop-down
      - Any, Default, or named connections will appear here
  - name: Scene Name
    type: Select
    required: false
    description: |
      Here you can specify a scene name if you only want it to trigger this event when you switch to a specific scene. If you leave this field empty it will trigger on every scene.
variables:
  - name: obs.id
    type: string
    description: The connection id
  - name: obs.name
    type: string
    description: The name of the connection
    value: Main OBS
  - name: obs.host
    type: string
    description: The IP Address of the OBS connection
    value: 127.0.0.1
  - name: obs.studioVersion
    type: string
    description: The current OBS Studio version
    value: 30.0.0
  - name: obs.websocketVersion
    type: string
    description: The current OBS websocket version
    value: 5.1.0
  - name: obs.sceneName
    type: string
    description: The new scene name
    value: Main scene
  - name: obs.oldSceneName
    version: 0.2.5
    type: string
    description: The previous scene name
    value: Previous Scene
---
