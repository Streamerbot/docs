---
title: Streaming
description: Change your streaming status
parameters:
  - name: ObsConnection
    type: Select
    required: true
    description: |
      Select the Connection from the drop-down
      - Any, Default, or named connections will appear here
  - name: State
    type: Select
    required: true
    description: |
      Choose the streaming state

      - `Start`: Start your streaming
      - `Stop`: Stop your streaming
variables: []
csharpMethods:
  - ObsStopStreaming
  - ObsStartStreaming
---