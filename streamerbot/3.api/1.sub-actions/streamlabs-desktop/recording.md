---
title: Recording
description: Change your current recording status
parameters:
  - name: Connection
    import: streamlabs-desktop/connection
  - name: State
    type: Select
    description: Select the desired recording state
    options:
      - value: Start
        description: Start recording
      - value: Stop
        description: Stop recording
      - value: Pause
        description: Pause recording
      - value: Resume
        description: Resume recording
variables: []
csharpMethods:
  - SlobsStopRecording
  - SlobsStartRecording
  - SlobsPauseRecording
  - SlobsResumeRecording
---
