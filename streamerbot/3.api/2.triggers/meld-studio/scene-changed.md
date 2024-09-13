---
title: Meld Studio Scene Changed
description: Trigger for when the Scene is changed in Meld Studio
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
  - name: meldStudio.sceneName
    type: string
    description: The current scene in Meld Studio
    value: Scene 4
  - name: meldStudio.oldSceneName
    type: string
    description: The previous scene in Meld Studio
    value: Scene 2
---

## Parameters
::field-group
  ::field{name=Connection type=Select required}
    Choose a configured Meld Connection
    - Select `Any` to trigger on any connection
  ::
  ::field{name=Scene Name type=Text required}
    Here you can specify a scene name if you only want it to trigger this event when you switch to a specific scene. If you leave this field empty it will trigger on every scene.
  ::
::
