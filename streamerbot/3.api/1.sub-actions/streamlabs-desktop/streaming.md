---
title: Streaming
description: Change your streaming status
parameters:
  - name: SlobsConnection
  - name: State
    type: Select
    required: true
    description: |
      Select the desired streaming state

      - `Start`: Start streaming
      - `Stop`: Stop streaming
csharpMethods:
  - SlobsStartStreaming
  - SlobsStopStreaming
---
