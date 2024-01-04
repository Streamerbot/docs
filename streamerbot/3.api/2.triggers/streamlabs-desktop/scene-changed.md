---
title: Streamlabs Desktop Scene Changed
navigation.title: Scene Changed
description: Trigger for when the Streamlabs Desktop Scene is Changed
version: 0.2.3
variables:
  - name: sd.id
    type: string
    description: The connection id
  - name: sd.name
    type: string
    description: The name of the connection
    value: Main
  - name: sd.host
    type: string
    description: The IP Address of the Streamlabs Desktop connection
    value: 127.0.0.1
  - name: sd.sceneName
    type: string
    description: The new scene name
    value: Scene Changed
---

## Parameters
::field-group
  ::field{name=Instance type=Select}
    Choose a configured Streamlabs Desktop Connection
    - Select `Any` to trigger on any connection
  ::
  ::field{name="Scene Name" type=Text}
    Here you can specify a scene name if you only want it to trigger this event when you switch to a specific scene. If you leave this field empty it will trigger on every scene.
  ::
::