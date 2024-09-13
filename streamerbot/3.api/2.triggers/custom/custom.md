---
title: Custom
description: Trigger for a Custom Event
version: 0.2.0
parameters:
  - name: Event Name
    type: string
    description: |
      Input the event name of the custom event

      - Leaving this blank is considered a catch-all and will trigger on **any** custom event
csharpMethods:
  - TriggerEvent
---

## Details
This event can **only** be triggered with the [`CPH.TriggerEvent`](#csharp-usage) C# Method.

## Variables
Variables are dependent on the custom event.