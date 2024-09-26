---
title: Recording
description: Change your current recording status
parameters:
  - name: SlobsConnection
  - name: State
    type: Select
    description: |
      Select the desired recording state

      - `Start`: Start recording
      - `Stop`: Stop recording
      - `Pause`: Pause recording
      - `Resume`: Resume recording
variables: []
csharpMethods:
  - SlobsStopRecording
  - SlobsStartRecording
  - SlobsPauseRecording
  - SlobsResumeRecording
---
