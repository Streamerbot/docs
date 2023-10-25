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

Next we have 2 check boxes `Include All` and `Only Has Permission`

`Include all` option will display all the commands in the specified group regardless of the permissions that have been set but, when paired with the `Only Has Permission` option checked it will only store the commands the user is permitted to use in that variable you have named.

> **Please Note:** The `Include All` checkbox on the sub action overrides the `Include` behaviour on the command itself and will list everything from the group you have selected. There may be commands you don't want to list to the user such as test commands. So be mindful of this.
{.is-info}

If you do enable the option `Only has permission` make sure at the beginning of the sub action you perform the 'Get User Info for Target' sub action and place it at the top of the sub action list. This is so the Streamer.bot can see if the user that redeemed it is a VIP/Moderator/Subscriber/Viewer and match it to the permissions that has been set on that command.

Lastly create a sub action to output the contents of the variable that is storing the commands. Again right click in the sub action section click `Add Action` then `Twitch` then `Send Message to Twitch Channel`. In here you would type a message and include the variable you named earlier.
> **For example : "/me These are the commands available to you: %commands%"**

![get_commands_sub_action_list_.png](/commands/get_commands_sub_action_list_.png =700x)

This is one example you can import to get started.

## Import Code
```
TlM0RR+LCAAAAAAABACVVE1vnDAQvVfqf7CQclu3BoOB3FY59FZVVW5VDsYeZ5EMbGy8ySrKfy+GRXztSskJe974ed4bD+/fvyEUnMDYsqmDexTu+kDNK+h2QTBsuWg72HaRf36P0Pvw6aBS+jxGIQ15nuJMhhzHMs+7VUFxqiCLwkTlBciBqz/04sB5/tppPUWh5oUGz9caB1N8LOahqSpeSzsjejaNO97AuH7lZ/vXeVmKaztjNF1qU+17VVtUNLVwxkDdbrGNEws3ljXttZ7K6aETN6XX+PuiSGyqHjythXYS/PmVFz184PYPmKq0l55tM4amCMZJQaTEjNMEx6liOCcxxUwIBYUUWSb46uZXKJ8PXjb5QZZIez76kkMS0nWxEt48MkU/dre8aeHNswc/K0CPB7CAuAHUHgCNViB+4qX2JqG2QefG3SN0N4J3q3KPBhR0nZJ7IRrX94tcc4LmcUyAAWZURjiOshDnImM4kkokImE0idnXndhdbfviTS8cij7jkG2cEfA43EGuP59pMlc6VRbTUGQUR5GSOA6THPOoG0ipICIUFEvJl3UmN3RuKrioJDOV4/JpPUC/PEk/RU/zudOaHy3IGTqAPdGQOfw7RvDjP2NyCCfABAAA
```

## Variables
This sub-action populates 2 variables with the custom name you specify, one as a string and one as a list

Name | Description
----:|:------------
`<variableName>` | Comma separated string containing all commands matching criteria specified in the sub-action
`<variableName>.List` | List object for C# containing all commands matching criteria specified in the sub-action

---

- [<i class="mdi mdi-chevron-left"></i> **Commands Sub-Actions Reference *Go Back***](/Sub-Actions/Commands)
{.btn-grid .my-5}