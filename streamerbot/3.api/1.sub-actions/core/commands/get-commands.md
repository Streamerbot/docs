---
title: Get Commands
description: Fetch a list of all configured commands
parameters:
  - name: Group
    type: Select
    required: true
    description: The command group to get commands from. Use "All" to get commands from all groups.
    default: 'All'
  - name: Variable Name
    type: Text
    required: true
    description: The variable name to store the resulting commands in.
  - name: Include All
    type: Toggle
    description: Include all commands regardless of their `Include` option checked or not.
    default: false
  - name: Only Has Permission
    type: Toggle
    description: Only get commands for which the user has permissions.
    default: false
  - name: Ignore Aliases
    type: Toggle
    description: When checked it will only use the first command alias you have defined in the command settings.
    default: false
variables:
  - name: '<variableName>'
    type: string
    description: Comma-separated string containing all commands matching your specified criteria
    value: '!shoutout,!followage,!ban'
  - name: '<variableName>List'
    type: List
    description: C# List object containing all commands matching your specified criteria
csharpMethods:
  - GetCommands
---

This sub-action is useful if you want to output a list of commands to your chat.

::warning
The Get Commands sub-action will not include commands that have their location set to `Anywhere`
::

### Handling Long Command Lists

:streamerbot-import{code="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"}


Since Twitch has a message character limit of 500 and on YouTube it's 200 you may find your commands overtake this amount therefore the code below can help with splitting the list into batches of commands that fit inside the messages.

```cs [Split Commands Example.cs]
using System;
using System.Collections.Generic;

public class CPHInline
{
    public bool Execute()
    {
        // This is when the Variable Name in the Get Commands Sub-Action is `commands`
        CPH.TryGetArg("commandsList", out List<string> commands);
        // Limit is 500 on Twitch, 200 on YouTube.. I took a few off as a safety measure.
        const int maxMessageLength = 495;
        string message = "Commands Avaliable to you: ";
        const string additionalCommandsMessage = "Addional Commands for you: ";
        const string commandSeparator = ", ";
        const bool sendFromBot = false;

        int commandsSent = 0;
        while (commandsSent < commands.Count)
        {
            int currentMessageLength = message.Length;
            bool fitsInMessage(string text) => currentMessageLength + text.Length < maxMessageLength;
            List<string> commandsForMessage = [];
            for (int i = commandsSent; i < commands.Count && fitsInMessage(commands[i]); i++)
            {
                commandsForMessage.Add(commands[i]);
                currentMessageLength += commands[i].Length + commandSeparator.Length;
            }

            message += string.Join(commandSeparator, commandsForMessage);
            // if you wish to send the message to Youtube, use CPH.SendYouTubeMessage(message, sendFromBot);
            CPH.SendAction(message, sendFromBot);
            commandsSent += commandsForMessage.Count;
            message = additionalCommandsMessage;
        }
        return true;
    }
}
```
