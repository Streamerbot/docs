---
title: Recording
description: Change your OBS recording status
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: State
    type: Select
    required: true
    description: Choose the recording state
    options:
      - value: Start
        description: Start your recording
      - value: Stop
        description: Stop your recording
      - value: Pause
        description: Pause your recording
      - value: Resume
        description: Resume your recording
variables: []
csharpMethods:
  - ObsStartRecording
  - ObsStopRecording
  - ObsPauseRecording
  - ObsResumeRecording
---