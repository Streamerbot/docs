---
title: Execute C# Code
description: Sub-action for writing advanced custom actions with C# code
---

::callout{icon=i-mdi-bookmark color=green to=/guide/csharp}
Learn more about custom code actions at [Guide > C# Code Actions](/api/csharp)
::

::callout{icon=i-mdi-bookmark color=green to=/api/csharp}
Explore all available C# methods at [API References > C# Methods](/api/csharp)
::

## Views
### Compiling Log
Shows some general information based on what buttons you've pressed, this will show any compiler errors, and general information when trying to find references

### References
List the references required for compiling your code.

::tip{color=amber}
You can :shortcut{value=Right-Click} within the pane if you need to add specific references
::

## Configuration
Configuration options available under the `Settings` tab are outlined below:

::field-group
  ::field{name=Name type=Text}
    Optionally set a descriptive name for your C# sub-action.

    ::tip{color=amber}
    `Name` is required if you would like to execute custom methods with the [Execute C# Method](/api/sub-actions/core/csharp/execute-csharp-method) sub-action.
    ::
  ::

  ::field{name=Description type=Text}
  Optionally set a longer description detailing what your C# sub-action does.
  ::

  ::field{name="Keep Instance Active" type=Toggle}
    By ticking this option, your code will be kept alive for the lifetime of the Streamer.bot application.

    This will allow you to **preserve data between calls** to this sub-action.

    ::tip
    As of Streamer.bot v0.2.3, this option has been removed and is enabled by default.
    ::
  ::

  ::field{name="Precompile on Application Start" type=Toggle}
  By ticking this, your code will be automatically compiled when you start Streamer.bot so it is ready to go, instead of the first time the sub-action is executed.
  ::

  ::field{name="Delayed Start" type=Toggle}
  When `Precompile on Application Start` is enabled, delay compilation until later in the startup routine.

  This is useful if you are **implementing UI** within your C# sub-action.
  ::

  ::field{name="Save Result to Variable" type=Toggle}
    Save the `bool` result of the `Execute()` method

    ::tip{color=amber}
    Returning `false` without this option enabled will simply stop execution of the entire action. Enabling this option allows you to collect the result and also continue execution regardless of the return value.
    ::
  ::

  ::field{name="Variable Name" type=Text}
  When `Save Result to Variable` is enabled, enter the name for the resulting variable here.
  ::
::

## Actions

::field-group
  ::field{name="Format Document" type=Button}
  Automatically format your code with proper indentation
  ::

  ::field{name="Find Refs" type=Button}
  Attempt to automatically find some common references based on your `using` directives.
  ::

  ::field{name="Compile" type=Button}
    Test the compilation of your code and check for errors.

    ::callout{icon=i-mdi-alert color=amber}
    This will also remove any references that are currently unused.
    If your code is stil in-progress, it could end up removing a reference that is actually needed.
    ::
  ::

  ::field{name="Save and Compile" type=Button}
  This will save your changes, and pre-compile the code so it's ready to go the first time the action is hit
  ::

  ::field{name="Ok" type=Button}
  Save your changes
  ::

  ::field{name="Cancel" type=Button}
  Discard your changes
  ::
::