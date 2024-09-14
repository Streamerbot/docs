---
title: Set Replay Buffer State
description: Change your replay buffer status
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
      Choose the replay buffer state

      - `Start`: Start your replay buffer
      - `Stop`: Stop your replay buffer
      - `Save`: Save your replay buffer
variables: []
csharpMethods:
  - ObsReplayBufferStart
  - ObsReplayBufferStop
  - ObsReplayBufferSave
---