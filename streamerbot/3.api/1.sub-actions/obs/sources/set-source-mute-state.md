---
title: Set Source Mute State
description: Mute or unmute a source
variables: []
csharpMethods:
  - ObsSetSourceMuteState
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  ::field{name=State type=Select required}
    Select the mute status for the source

    - `Muted`: Set the mute state to muted
    - `Not Muted`: Set the mute state to not muted
    - `Toggle`: Toggle the mute state between muted and not muted
  ::
::