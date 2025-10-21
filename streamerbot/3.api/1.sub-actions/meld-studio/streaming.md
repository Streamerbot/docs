---
title: Streaming
description: Change your Meld Studio streaming status
version: 0.2.5
parameters:
  - name: Connection
    import: meld-studio/connection
  - name: State
    type: Select
    required: true
    description: Choose the streaming state
    options:
      - value: Start
        description: Start streaming
      - value: Stop
        description: Stop streaming
      - value: Toggle
        description: Toggle your streaming status
variables: []
---
