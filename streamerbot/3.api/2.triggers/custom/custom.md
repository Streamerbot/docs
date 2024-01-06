---
title: Custom
description: Trigger for a Custom Event
version: 0.2.0
csharpMethods:
  - TriggerEvent
---

## Details
This event can **only* be triggered with the [`CPH.TriggerEvent`](#csharp-usage) C# Method.

## Parameters
::field-group
  ::field{name="Event Name" type=Text}
    Input the event name of the custom event

    - Leaving this blank is considered a catch-all and will trigger on **any** custom event
  ::
::

## Variables
Variables are dependent on the custom event.