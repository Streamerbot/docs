---
title: OBS Scene Changed
description: Trigger for when an OBS Scene is Changed
version: 0.2.0
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
---

## Parameters
::field-group
  ::field{name=OBS type=Select}
    Choose a configured OBS Connection
    - Select `Any` to trigger on any connection
  ::
  ::field{name="Scene Name" type=Text}
    Here you can specify a scene name if you only want it to trigger this event when you switch to a specific scene. If you leave this field empty it will trigger on every scene.
  ::
::