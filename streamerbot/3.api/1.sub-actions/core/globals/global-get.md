---
title: Get Global Variable
description: Fetch the value of a global variable and populate a local argument
variables:
  - name: <variableName>
    description: The variable name and type will be depend on the parameters you selected
csharpMethods:
  - GetGlobalVar
---

::tip
You can quickly access persisted globals without this sub-action by wrapping the name with `~`<br>
:icon{name=i-mdi-chevron-right} `~myGlobalVariable~`{lang=cs}
::

:read-more{to=/guide/variables}

## Parameters
::field-group
  ::field{name=Source type=Select default="Global" required}
    Select the source type for the global variable

    - `Global` - Fetch any general global variable (non user variables)
    - `User (redeemer)` - Fetch a user global for the current user who **activated** the action
    - `User (target)` - Fetch a user global for the `targetUser`
        - Used in conjunction with the [Get User Info for Target](/api/sub-actions/twitch/user/get-user-info-for-target) sub-action
  ::

  ::field{name=Persisted type=Toggle default=true}
    Toggle between `Persisted` and `Non-Persisted` variables

    - `Persisted` - These variables persist across Streamer.bot restarts
    - `Non-Persisted` - These variables should be considered **temporary** and will be wiped at shutdown

    ::warning
    Ensure you select the correct datastore (persisted or non-persisted) for the variable you are trying to fetch
    ::
  ::

  ::field{name="Variable Name" type=Text required}
    Enter the name of the variable you would like to fetch

    ::warning
    `Variable Name` must be entered in `camelCase` (the first letter must be lowercase)
    ::
  ::

  ::field{name="Destination Variable" type=Text required}
    Enter the name of the local argument you would like to populate

    ::tip
    It is recommended to use a **differet name** than the global variable name
    ::
  ::

  ::field{name="Default Value" type=Text}
    Optionally set a default value to apply if the global variable does not exist

    ::tip
    This will also set the value of the global variable
    ::
  ::
::