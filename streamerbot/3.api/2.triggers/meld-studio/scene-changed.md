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
  ::field{name=Scene Name type=Input required}
    Type the name of the scene to trigger an event
    - Leave `Blank` to trigger on any Scene Change
  ::
::
