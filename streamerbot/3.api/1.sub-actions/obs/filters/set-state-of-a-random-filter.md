---
title: Set State of a Random Filter
description: Set the state of a random filter
variables: []
csharpMethods:
  - ObsSetRandomFilterState
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  ::field{name=State type=Select required}
    Select the state for the random filter

    - `Visible`: Set the filter state to visible
    - `Hidden`: Set the filter state to hidden
    - `Toggle`: Toggle the filter state between visible and hidden
  ::
::