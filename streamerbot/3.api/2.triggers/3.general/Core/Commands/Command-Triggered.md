# Command Triggered
Command Triggered trigger.

## Details
This event triggers when a command is triggered.

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
`msgId` | The unique message id for this message
`rawInput` | The message entered, if the command was a Starts With, this will be removed 
`rawInputEscaped` | The message escaped
`rawInputUrlEncoded` | The message URL encoded
`input#` | The # word of the message entered, spaces are delimiters and variable names are 0 indexed, so `input0` would give the first word, `input1` would give the second, and so on
`inputEscaped#` | The indexed word escaped
`inputUrlEncoded#` | The indexed word URL encoded
`role` | What role the user has `(1-4)` <br> 4=`Broadcaster` 3=`Mod` 2=`VIP` 1=`Viewer`
`counter` | A running total of how many times a command has been run since application launch (if 

:variables{name=TwitchUser disclosure}
:variables{name=TwitchBroadcaster disclosure}