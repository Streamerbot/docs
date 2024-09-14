---
title: Get Status
description: Get your OBS Studio output status
parameters:
  - name: ObsConnection
    type: Select
    required: true
    description: |
      Select the Connection from the drop-down
      - Any, Default, or named connections will appear here
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