---
title: General Variables
navigation.title: General
description: Variables available for all action executions
variables:
  - name: actionId
    type: Guid
    description: The unique ID of the action being executed
    value: 2cd1495a-e50c-45d2-8bb5-ffe9c3dff243
  - name: actionName
    type: string
    description: The name of the action being executed
    value: My Action
  - name: runningActionId
    type: Guid
    description: The unique ID of this running action instance within the queue
    value: c83dd939-9f86-4435-b07c-b6e7e3eef134
  - name: actionQueuedAt
    type: DateTime
    description: The timestamp of when action was queued
    value: 12/21/2023 9:25:21 AM
  - name: triggerId
    type: Guid
    description: The unique id of the trigger with executed the action
    value: 2cd1495a-e50c-45d2-8bb5-ffe9c3dff243
  - name: triggerName
    type: string
    description: The name of the trigger which executed the action
    value: Chat Message
  - name: triggerCategory
    type: string
    description: The category of the trigger which executed the action
    value: Twitch/Chat
  - name: __source
    type: EventType
    description: The event which triggered the action. <br>_This will not always exist and requires C# to access, [read more](/api/csharp/core/events)_
    value: TwitchChatMessage
  - name: eventSource
    type: EventSource
    description: The service of the event which triggered the action. <br>_This will not always exist and requires C# to access, [read more](/api/csharp/core/events)_
    value: twitch
---
