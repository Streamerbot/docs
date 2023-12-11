---
title: Get Commands
description: Commands Sub-Actions Reference
published: true
date: 2023-04-07T22:04:32.578Z
tags: twitch, commands, chat
editor: markdown
dateCreated: 2022-02-27T00:38:17.197Z
---

This sub action allows you to populate the commands and output them to your twitch chat. Just like the one below
![get_all_commands_output_.png](/commands/get_all_commands_output_.png =600x)

To do this all you need to do is create an action and give it a name next go to the sub action window on the right and then right click to get the option menu to open now navigate through the following `Add Action` then `Commands` then click the `Get Commands` Option. Just like the image below.
![commands_menu.png](/commands/commands_menu.png =600x)

Once you have done this a dialog box will appear from here you can select the group of commands you want to be outputted to the user that requested the commands list in your twitch chat. Various options will be displayed depending on how you have grouped your commands in the Commands tab.
> Note: Due to a limitation on Twitch if your total commands exceed 500 Characters the message to the Twitch chat will **NOT** be sent!!!
{.is-info}

Next field we have is a variable name field here you will need to input a name for all the commands populated to be stored in ready for you to call in a Send to Twitch channel action. So enter a name and remember it. We will need this later.

![dialog_-group_options_.png](/commands/dialog_-group_options_.png =350x) ![example_catergory_.png](/commands/example_catergory_.png =350x)

Next we have 3 check boxes `Include All`, `Ignore Aliases` and `Only Has Permission`

`Include all` option will display all the commands in the specified group regardless of the permissions that have been set but, when paired with the `Only Has Permission` option checked it will only store the commands the user is permitted to use in that variable you have named.

> **Please Note:** The `Include All` checkbox on the sub action overrides the `Include` behaviour on the command itself and will list everything from the group you have selected. There may be commands you don't want to list to the user such as test commands. So be mindful of this.
{.is-info}

`Ignore Aliases` option will give you the chance to hide any of your commands other formats for example if you have `!shoutout` and `!so` in the commands box it will only show the 1st one having this option unticked would show both when populating the list.

If you do enable the option `Only has permission` make sure at the beginning of the sub action you perform the 'Get User Info for Target' sub action and place it at the top of the sub action list. This is so the Streamer.bot can see if the user that redeemed it is a VIP/Moderator/Subscriber/Viewer and match it to the permissions that has been set on that command.

Lastly create a sub action to output the contents of the variable that is storing the commands. Again right click in the sub action section click `Add Action` then `Twitch` then `Send Message to Twitch Channel`. In here you would type a message and include the variable you named earlier.
> **For example : "/me These are the commands available to you: %commands%"**

![get_commands_sub_action_list_.png](/commands/get_commands_sub_action_list_.png =700x)

This is one example you can import to get started.

## Import Code
```
U0JBRR+LCAAAAAAABACtVclu2zAQvQfIPxACcgtdSZRkKTej66VFUQS5FD1Q5MgmIIkuSSU2gvx7SS3eJBdG4Jv43miWNzPk6+0NQt4zKC1k7T0gct8ColpLZZ52cNjBlahF1VR73PNn4Sz0ehYMtdirO9hjTStwJt+36PPGuevMLEMbs5LKcY+glAD1iSqjd/Q+Gy+Y+TN/R3DQTIm16UnPwW9dbE6PYlPmjLRFfncIGqiWFtz9nxCYBzSb45QHFEc8y+xXTvC8gDQM4iLLgQ+x29/+NtC4kuqmLA9xqGlegvNpVANHzIaVDYcvSlbfhDZSba1RQUt9ZDUo9VFWFa25Pgq6VLJZn2Vp+UK3+ldTT/lV1lxWC9YLNuKZrFmjFNRmijVKLJe2FU7EP0cxx+KeCLxP/EdX2oliXZupEk633sRmM66v61bdirgoy7HCncGylsrygmrQE6W0Riuqf4KqhO5na9JROxcsoX7uc44TSmIczYsEZ35EcMJYATlnacroKMkXEMuV09EO7ClntmtXYeAH5JTadddVd0qenateFg4b5/YQf7v/X0sMbFyK3ocK0OMKNCCqAJkVoEF8RJ+pKF1YZCTayuYBobuBvBtluFZQ2BUGvmBMNu0cjarvRCVZFPmQAE4ID3EUpgHOWJrgkBcsZnFC4ih5n6jnJJ2aucsUDS9XVMtGMXjsczk34u1tNa1LkUYkYCnBYVhwHAVxhmloryNeQOgTKJK5/y5d4rO6jDO5TBX/clUOV39yst+3+5N7feXlj3mUxzwLMIXcd8uf4izOEkwyzgid+zHE5OrLf5XN3x8mbuuvLtT4KmeyLOlaAz/gB7p3ONh3r9+Ri33bDkEjquHVaB/o25u3f/fC+E1mCAAA
```

## Variables
This sub-action populates 2 variables with the custom name you specify, one as a string and one as a list

Name | Description
----:|:------------
`<variableName>` | Comma separated string containing all commands matching criteria specified in the sub-action
`<variableName>List` | List object for C# containing all commands matching criteria specified in the sub-action

## CSharp Example

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
                CPH.SendMessage(message, bot); // This will need to be changed to CPH.SendYouTubeMessage(message, bot); if you wish to send the message to Youtube
                message = "Addional Commands for you: ";
            }

            message += commands[i] + ", ";
        }
        CPH.SendMessage(message, bot); // This will need to be changed to CPH.SendYouTubeMessage(message, bot); if you wish to send the message to Youtube
        return true;
    }
}
```  

---

- [<i class="mdi mdi-chevron-left"></i> **Commands Sub-Actions Reference *Go Back***](/Sub-Actions/Commands)
{.btn-grid .my-5}