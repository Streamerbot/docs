---
title: Get Status
description: Get your OBS Studio output status
variables:
  - name: obs.isConnected
    type: boolean
    description: If the selected OBS connection is connected
    value: True
  - name: obs.isStreaming
    type: boolean
    description: If the selected OBS connection is streaming
    value: True
  - name: obs.isRecording
    type: boolean
    description: If the selected OBS connection is recording
    value: True
csharpMethods:
  - ObsIsConnected
  - ObsIsStreaming
  - ObsIsRecording
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
::