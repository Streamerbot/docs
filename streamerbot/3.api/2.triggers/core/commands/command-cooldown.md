---
title: Command Cooldown
description: Trigger for when a Command is on Cooldown
parameters:
  - name: Commands
    type: Select
    description: |
      Select the command to monitor for cooldowns

      ::tip
      You can quickly register a new command by clicking the `Create Command` button!
      ::
    required: true
variables:
  - name: command
    type: string
    description: The command that was used
    value: '!shoutout'
  - name: commandId
    type: Guid
    description: The id of the command
  - name: commandSource
    type: string
    description: The command source
    value: twitch
  - name: commandType
    type: string
    description: The type of the command
    value: message
  - name: cooldownLeft
    type: number
    description: How much seconds are left for the cooldown, and the maximum of the global and user cooldown
    value: 30
  - name: globalCooldownLeft
    type: number
    description: How much seconds are left for the global cooldown
    value: 15
  - name: userCooldownLeft
    type: number
    description: How much seconds are left for the user cooldown
    value: 30
commonVariables:
  - TwitchUser
  - TwitchBroadcaster
  - YouTubeUser
  - YouTubeBroadcaster
  - TrovoUser
  - TrovoBroadcaster
  - KickUser
  - KickBroadcaster
---

::read-more{to=/guide/commands}
Check out the [Commands Guide](/guide/commands) for details on configuring your Commands
::
