# Command Cooldown
Command Cooldown trigger.

## Details
This event triggers when a command is used whilst it is in cooldown.

## Parameters
### `Commands`
Select a command from the Commands tab.

## Variables
:variables-description

Name | Description
----:|:------------
`command` | The command that was used
`commandId` | The ID of the command
`commandSource` | The command source <br> `twitch`/`youtube`
`commandType` | The type of the command e.g. `message`
`cooldownLeft` | How many seconds are left for the cooldown, and is the maximum of the global and user cooldown left
`globalCooldownLeft` | How many seconds are left for the global cooldown of the command
`userCooldownLeft` | How many seconds are left for the user cooldown of the command

:variables{name=TwitchUser disclosure}
:variables{name=TwitchBroadcaster disclosure}