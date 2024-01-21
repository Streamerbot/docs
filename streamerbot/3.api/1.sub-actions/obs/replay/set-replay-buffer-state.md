---
title: Set Replay Buffer State
description: Change your replay buffer status
variables: []
csharpMethods:
  - ObsReplayBufferStart
  - ObsReplayBufferStop
  - ObsReplayBufferSave
---

:image-preview

## Parameters
::field-group
  :parameter{name=ObsConnection}
  ::field{name=State type=Select required}
    Choose the recording state

    - `Start`: Start your replay buffer
    - `Stop`: Stop your replay buffer
    - `Save`: Save your replay buffer
  ::
::