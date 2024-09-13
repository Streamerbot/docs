---
title: Meld Studio Set Effect Enabled State
description: Sets the enabled state of the selected effect in Meld Studio
version: 0.2.5
variables: []
---

## Parameters
::field-group
  :parameter{name=Connection}
  :parameter{name=Scene}
  :parameter{name=Layer}
  :parameter{name=Filter}
  ::field{name=State type=Select required}
    Select which state you want to set

    - `Visible`: Sets the effect state on your scene to Visible
    - `Hidden`: Sets the effect state on your scene to Hidden
    - `Toggle`: Toggles the effect state on your scene between Visible and Hidden
  ::
::
