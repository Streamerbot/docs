---
title: Set Replay Buffer State
description: Change your replay buffer status
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: State
    type: Select
    required: true
    description: Choose the replay buffer state
    options:
      - value: Start
        description: Start your replay buffer
      - value: Stop
        description: Stop your replay buffer
      - value: Save
        description: Save your replay buffer
variables: []
csharpMethods:
  - ObsReplayBufferStart
  - ObsReplayBufferStop
  - ObsReplayBufferSave
---