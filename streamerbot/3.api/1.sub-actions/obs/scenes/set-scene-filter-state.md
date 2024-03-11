---
title: Set Scene Filter State
description: Sets the visibility state of a scene filter
variables: []
csharpMethods:
  - ObsSetSceneFilterState
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsFilter}
  ::field{name=State type=Select required}
    Select which state you want to set

    - `Visible`: Sets the filter state on your scene to Visible
    - `Hidden`: Sets the filter state on your scene to Hidden
    - `Toggle`: Toggles the filter state on your scene between Visible and Hidden
  ::
::