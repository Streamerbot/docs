---
title: Streaming
description: Change your streaming status
parameters:
  - name: ObsConnection
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