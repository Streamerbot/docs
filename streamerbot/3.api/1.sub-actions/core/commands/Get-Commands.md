# Get Commands
This sub action allows you to populate the commands and output them to your twitch chat.

:image-preview

## Parameters
### `Group`
The name of the command group.

### `Variable Name`
The name of the variable that will be used when running the action. For example, if you use the variable name: "chatCommands". The following variables will be populated: `chatCommands`, `chatCommandsList`

### `Include all`
This option will display all the commands in the specified group regardless of the permissions that have been set for these commands.

### `Ignore Aliases`
This option will give you the chance to hide any of your commands other formats for example if you have `!shoutout` and `!so` in the commands box it will only show the 1st one having this option unticked would show both when populating the list.

### `Only Has Permission`
This option will filter out all the commands that the user doesn't has permission to use.

## Variables
:variables-description

Name | Description
----:|:------------
`<variableName>` | Comma separated string containing all commands matching criteria specified in the sub-action
`<variableName>List` | List object for C# containing all commands matching criteria specified in the sub-action

## C# Usage
:csharp-method

## Example Usage
### Import Code
```
U0JBRR+LCAAAAAAABACtVclu2zAQvQfIPxACcgtdSZRkKTej66VFUQS5FD1Q5MgmIIkuSSU2gvx7SS3eJBdG4Jv43miWNzPk6+0NQt4zKC1k7T0gct8ColpLZZ52cNjBlahF1VR73PNn4Sz0ehYMtdirO9hjTStwJt+36PPGuevMLEMbs5LKcY+glAD1iSqjd/Q+Gy+Y+TN/R3DQTIm16UnPwW9dbE6PYlPmjLRFfncIGqiWFtz9nxCYBzSb45QHFEc8y+xXTvC8gDQM4iLLgQ+x29/+NtC4kuqmLA9xqGlegvNpVANHzIaVDYcvSlbfhDZSba1RQUt9ZDUo9VFWFa25Pgq6VLJZn2Vp+UK3+ldTT/lV1lxWC9YLNuKZrFmjFNRmijVKLJe2FU7EP0cxx+KeCLxP/EdX2oliXZupEk633sRmM66v61bdirgoy7HCncGylsrygmrQE6W0Riuqf4KqhO5na9JROxcsoX7uc44TSmIczYsEZ35EcMJYATlnacroKMkXEMuV09EO7ClntmtXYeAH5JTadddVd0qenateFg4b5/YQf7v/X0sMbFyK3ocK0OMKNCCqAJkVoEF8RJ+pKF1YZCTayuYBobuBvBtluFZQ2BUGvmBMNu0cjarvRCVZFPmQAE4ID3EUpgHOWJrgkBcsZnFC4ih5n6jnJJ2aucsUDS9XVMtGMXjsczk34u1tNa1LkUYkYCnBYVhwHAVxhmloryNeQOgTKJK5/y5d4rO6jDO5TBX/clUOV39yst+3+5N7feXlj3mUxzwLMIXcd8uf4izOEkwyzgid+zHE5OrLf5XN3x8mbuuvLtT4KmeyLOlaAz/gB7p3ONh3r9+Ri33bDkEjquHVaB/o25u3f/fC+E1mCAAA
```

### C# Code
Since Twitch has a message charater limit of 500 and on YouTube it's 200 you may find your commands overtake this amount therefore the code below can help with splitting the list into batches of commands that fit inside the messages.

```cs
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