---
title: Recording
description: Change your recording status
parameters:
  - name: ObsConnection
  - name: State
    type: Select
    required: true
    description: |
      Choose the recording state

      - `Start`: Start your recording
      - `Stop`: Stop your recording
      - `Pause`: Pause your recording
      - `Resume`: Resume your recording
variables: []
csharpMethods:
  - ObsStartRecording
  - ObsStopRecording
  - ObsPauseRecording
  - ObsResumeRecording
---