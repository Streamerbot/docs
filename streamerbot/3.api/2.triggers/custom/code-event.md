---
title: Custom Code Event
description: Trigger for a Custom Code Event
version: 0.2.0
csharpMethods:
  - RegisterCustomTrigger
  - TriggerCodeEvent
---

## Details
This event can **only* be triggered with the [`CPH.TriggerCodeEvent`](#csharp-usage) C# Method. You can use two methods. With the first method you can use the variables of the current action. With the second method you can specify a dictionary of variables for the trigger.

When registering a trigger your trigger will end up in the `Custom` folder under triggers. You can nest the trigger in multiple folders by using the `catergories` parameter. To give the trigger a name use the `triggerName` parameter. Use the `eventName` parameter for a name only used in C# for triggering the method.

## Variables
Variables are dependent on the custom event.