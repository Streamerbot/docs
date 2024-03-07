---
title: Set Source Filter State
description: Sets the visibility state of a source filter
variables: []
csharpMethods:
  - ObsSetSourceFilterState
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  :parameter{name=ObsFilter}
  ::field{name=State type=Select required}
    Select which state you want to set

    - `Visible`: Sets the filter state on your scene to Visible
    - `Hidden`: Sets the filter state on your scene to Hidden
    - `Toggle`: Toggles the filter state on your scene between Visible and Hidden
  ::
::