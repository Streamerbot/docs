---
title: Meld Studio Layer Track Muted State
description: Mute or unmute a Track within a Layer in Meld Studio
variables: []
---

## Parameters
::field-group
  :parameter{name=Connection}
  :parameter{name=Scene}
  :parameter{name=Layer}
  :parameter{name=Track}
  ::field{name=State type=Select required}
    Select the mute status for the source

    - `Muted`: Set the mute state to muted
    - `Not Muted`: Set the mute state to not muted
    - `Toggle`: Toggle the mute state between muted and not muted
  ::
::
