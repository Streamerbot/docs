---
title: Streaming
description: Change your streaming status
variables: []
csharpMethods:
  - ObsStopStreaming
  - ObsStartStreaming
---

:image-preview

## Parameters
::field-group
  :parameter{name=ObsConnection}
  ::field{name=State type=Select required}
    Choose the streaming state

    - `Start`: Start your streaming
    - `Stop`: Stop your streaming
  ::
::