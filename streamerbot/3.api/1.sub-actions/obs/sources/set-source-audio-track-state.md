---
title: Set Source Audio Track State
description: Set the audio track state on a source
variables: []
csharpMethods: []
---

## Parameters
::field-group
  :parameter{name=ObsConnection}
  :parameter{name=ObsScene}
  :parameter{name=ObsSource}
  ::field{name=Track type=Select required}
    Select which audio track to change to

    - Options: `Track 1`, `Track 2`, `Track 3`, `Track 3`, `Track 5`, `Track 6`
  ::
  ::field{name=State type=Select required}
    Select an audio track state

    - `Active`: Sets the audio track state to Active
    - `Inactive`: Sets the audio track state to Inactive
    - `Toggle`: Toggles the audio track state between Active and Inactive
  ::
::