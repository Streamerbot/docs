---
title: Meld Studio Set Track Muted State
description: Mute or unmute a source
version: 0.2.5
variables: []
---

## Parameters
::field-group
  :parameter{name=Connection}
  :parameter{name=Scene}
  ::field{name=State type=Select required}
    Select the mute status for the source

    - `Muted`: Set the mute state to muted
    - `Not Muted`: Set the mute state to not muted
    - `Toggle`: Toggle the mute state between muted and not muted
  ::
::
