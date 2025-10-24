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
        List<string> commands = (List<string>)args["commandsList"];//This is when the Variable Name in the Get Commands Sub-Action is `commands`
        string message = "Commands Avaliable to you: ";
        bool bot = false;
        int messageMax = 495; //Limit is 500 on Twitch, 200 on YouTube.. I took a few off as a safety measure.
        for (int i = 0; i < commands.Count; i++)
        {
            if ((commands[i].Length + message.Length) > messageMax)
            {
                CPH.SendAction(message, bot); // This will need to be changed to CPH.SendYouTubeMessage(message, bot); if you wish to send the message to Youtube
                message = "Addional Commands for you: ";
            }

            message += commands[i] + ", ";
        }
        CPH.SendAction(message, bot); // This will need to be changed to CPH.SendYouTubeMessage(message, bot); if you wish to send the message to Youtube
        return true;
    }
}
```
