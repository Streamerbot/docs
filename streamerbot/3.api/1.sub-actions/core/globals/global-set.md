---
title: Set Global Variable
description: Create or update a global variable
variables: []
csharpMethods:
  - SetGlobalVar
---

:read-more{to=/guide/variables}

## Parameters
::field-group
  ::field{name=Destination type=Select default="Global" required}
    Select the destination type for the global variable

    - `Global` - Set a general global variable (non user variable)
    - `User (redeemer)` - Set a user global for the current user who **activated** the action
    - `User (target)` - Set a user global for the `targetUser`
        - Used in conjunction with the [Get User Info for Target](/api/sub-actions/twitch/user/get-user-info-for-target) sub-action
  ::

  ::field{name=Persisted type=Toggle default=true}
    Toggle between `Persisted` and `Non-Persisted` variables

    - `Persisted` - These variables persist across Streamer.bot restarts
    - `Non-Persisted` - These variables should be considered **temporary** and will be wiped at shutdown

    ::warning
    Ensure you select the correct datastore (persisted or non-persisted) for the variable you are trying to set
    ::
  ::

  ::field{name="Variable Name" type=Text required}
    Enter the name of the variable you would like to create or modify

    ::warning
    `Variable Name` must be entered in `camelCase` (the first letter must be lowercase)
    ::
  ::

  ::field{name="Source" type=Select default=Argument required}
    Select the source for the value to assign to the global variable

    - `Argument` - Use the value of an argument
    - `Value` - Assign any arbitrary value
    - `Increment` - Add to an existing `int`{lang=cs} variable
    - `Decrement` - Subtract from an existing `int`{lang=cs} variable
  ::

  ::field{name="Value" type=Text required}
  Enter the value to assign to the global variable, depends on the selected `Source` type, detailed above

  - `Argument` - Enter the name of an existing argument to assign its value to the global variable
  - `Value` - Enter any value
  - `Increment` - Enter any `int`{lang=cs}
  - `Decrement` - Enter any `int`{lang=cs}
  ::
::
