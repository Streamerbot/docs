---
title: Recording
description: Change your recording status
variables: []
csharpMethods:
  - ObsStartRecording
  - ObsStopRecording
  - ObsPauseRecording
  - ObsResumeRecording
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  ::field{name=State type=Select required}
    Choose the recording state

    - `Start`: Start your recording
    - `Stop`: Stop your recording
    - `Pause`: Pause your recording
    - `Resume`: Resume your recording
  ::
::