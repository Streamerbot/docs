---
title: Command Triggered
description: Trigger for when a Command is Triggered
variables:
  - name: command
    type: string
    description: The command that was used
    value: '!shoutout'
  - name: commandId
    type: string
    description: The ID of the command
  - name: commandSource
    type: string
    description: The command source
    value: twitch
  - name: commandType
    type: string
    description: The type of the command
    value: message
  - name: msgId
    type: string
    description: The unique message id for this message
  - name: rawInput
    type: string
    description: The message entered, if the command was a Starts With, this will be removed
  - name: rawInputEscaped
    type: string
    description: The message escaped
  - name: rawInputUrlEncoded
    type: string
    description: The message URL encoded
  - name: input#
    type: string
    description: The `#` word of the message entered, spaces are delimiters and variable names are 0 indexed, so `input0` would give the first word, `input1` would give the second, and so on
  - name: inputEscaped#
    type: string
    description: The indexed word escaped
  - name: inputUrlEncoded#
    type: string
    description: The indexed word URL encoded
  - name: role
    type: number
    description: What role the user has<br>1=`Viewer`, 2=`VIP`, 3=`Mod`, 4=`Broadcaster`
  - name: counter
    type: number
    description: A running total of how many times a command has been run since application launch
    value: 17
commonVariables:
  - TwitchUser
  - TwitchBroadcaster
  - YouTubeUser
  - YouTubeBroadcaster
  - TrovoUser
---

::callout{icon=i-mdi-bookmark to=/guide/commands}
Check out the [Commands Guide](/guide/commands) for details on configuring your Commands
::

## Parameters
::field-group
  ::field{name=Commands type=Select}
    Select a command from the Commands tab.

    ::tip{color=amber}
    You can quickly register a new command by clicking the `Create Command` button!
    ::
  ::
::