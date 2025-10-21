---
title: Streaming
description: Change your streaming status
parameters:
  - name: Connection
    import: streamlabs-desktop/connection
  - name: State
    type: Select
    required: true
    description: Select the desired streaming state
    options:
      - value: Start
        description: Start streaming
      - value: Stop
        description: Stop streaming
csharpMethods:
  - SlobsStartStreaming
  - SlobsStopStreaming
---
