---
title: Streaming
description: Change your streaming status
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: State
    type: Select
    required: true
    description: Choose the streaming state
    options:
      - value: Start
        description: Start your streaming
      - value: Stop
        description: Stop your streaming
variables: []
csharpMethods:
  - ObsStopStreaming
  - ObsStartStreaming
---