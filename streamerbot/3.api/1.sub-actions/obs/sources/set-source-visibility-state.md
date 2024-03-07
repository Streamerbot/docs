---
title: Set Source Visibility State
description: Show or hide a source
variables: []
csharpMethods:
  - ObsSetSourceVisibility
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  ::field{name=State type=Select required}
    Select the state for the source visibility state

    - `Visible`: Set the visibility state to visible
    - `Hidden`: Set the visibility state to hidden
    - `Toggle`: Toggle the visibility state between visible and hidden
  ::
::