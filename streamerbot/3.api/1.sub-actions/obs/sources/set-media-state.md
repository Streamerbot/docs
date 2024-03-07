---
title: Set Media State
description: Set the status of the media source
variables: []
csharpMethods:
  - ObsSetMediaState
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  ::field{name=State type=Select required}
    Select on which side you want to flip the source

    - `Play`: Play your Media Source
    - `Pause`: Pause your Media Source
    - `Restart`: Restart your Media Source
    - `Stop`: Stop your Media Source
    - `Next`: Go next on your Media Source
    - `Previous`: Go to the previous on your Media Source
  ::
::