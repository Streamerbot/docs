---
title: Execute C# Method
description: Sub-action for directly calling a method defined in another C# code sub-action
---

::callout{icon=i-mdi-bookmark color=green to=/guide/csharp}
Learn more about custom code actions at [Guide > C# Code Actions](/api/csharp)
::

Using this sub-action you can directly call into methods defined in your existing [Execute C# Code](/api/sub-actions/core/csharp/execute-csharp-code) sub-actions.

Custom methods must be in the form of a return type of `bool` with no parameters:

```csharp [Example]
public bool MethodName()
{
  // your code here
  return true;
}
```

::tip{color=amber}
  If you have the selected `Execute C# Code` sub-action setup for `Keep Alive` and `Precompile on Startup` you can use `private` variables within the class to **preserve data between calls**.
::

## Configuration

::field-group
  ::field{name="Execute C# Code" type=Select}
    Select the `Execute C# Code` sub-action you would like to reference.

    ::tip{color=amber}
    You must configure the `Name` field in your `Execute C# Code` sub-actions to display here. [Read more](/api/sub-actions/core/csharp/execute-csharp-code#configuration)
    ::
  ::

  ::field{name=Method type=Select}
    Select the method to execute

    ::tip{color=amber}
    This can be any custom defined method, or even the main `Execute()` method.
    ::
  ::

  ::field{name="Run on UI Thread" type=Toggle}

  ::

  ::field{name="Save Result to Variable" type=Toggle}
    Save the `bool` result of the selected method

    ::tip{color=amber}
    Returning `false` without this option enabled will simply stop execution of the entire action. Enabling this option allows you to collect the result and also continue execution regardless of the return value.
    ::
  ::

  ::field{name="Variable Name" type=Text}
  When `Save Result to Variable` is enabled, enter the name for the resulting variable here.
  ::
::