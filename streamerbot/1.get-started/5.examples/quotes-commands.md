---
title: Quotes Commands for v1.0.0+
description: An example how to get and add quotes using commands in Streamer.bot v1.0.0+
author: pwnyy
icon: i-mdi-format-quote-close
navigation: false
difficulty: 1
---

::warning
This is only for Streamer.bot v1.0.0 and above!
::

In Streamer.bot v1.0.0+, the built-in quote command "!quote" has been removed. This allows for more customization and flexibility in how quotes are retrieved and displayed. With that the "Show Quote" trigger will also not work anymore.
The following example shows how to create your own "!quote" command to either retrieve a random quote or a specific quote by its index. 

An import is provided at the end of the instructions, which includes a "!quote" and "!quoteadd" command.

The instructions below will guide you through the process of creating a quote command that can retrieve quotes, and add new quotes.
Keep in mind this is just an example, and you can customize the sub-actions to your liking. The following sub-actions will be used to retrieve a random quote or a specific quote by its index. It will also be checked whether or not a command input is a number or not via inline math.

## Instructions (Get Quote)

1. Creating an action

    To create a new action head to the **Actions** tab and right-click in the actions section. Select **Add Action** and name it something like "Get Quote". This action will be used to retrieve a random quote or a specific quote by its index.

2. Adding the "!quote" command trigger

    Next step would be adding our trigger for the command. Right-click in the **Triggers** section and select `Core -> Commands -> Command Triggered`.
    If you already have a command like "!quote" and want to use that, you can select it from the dropdown menu. If not, you can create a new command by clicking on the `Create Command` button below the dropdown.

    Give the command a name like "Get Quote" and set the command itself to `!quote`, or anything you like.
    Leave the location to `Start`, this will allow the command to also check an input.

    The other settings can be left as is, unless you want to change them. For example, you can set the `Cooldown` to prevent spamming the command.

    ![Add Quote Command](assets/quote-command-get-quote.png)

3. Check whether input is  empty or not
    First we want to check whether the input, in our case the argument `input0` is empty or not. If it is empty, we will retrieve a random quote, otherwise we will try to retrieve a specific quote by the input.
    To do this, we will use an the sub-action `Core -> Logic > If/Else`.

    - In the Input field you would write `%input0%` to get the value of the input0 argument.
    - The Operation would be `Is Null or Empty`.

    After clicking `OK`, you will see a new If/Else block in your action. In the `True` group, we will retrieve a random quote, and in the `False` group we will try to retrieve a specific quote by its index.
    ![Check if empty](assets/quote-if-empty.png)
4. Get a random quote and send the message

    In the `True` group of the If/Else block, we will retrieve a random quote.
    To do this, right-click on the `True Result` group and add the sub-action `Core -> Quotes -> Get Quote`.
    Or you can also click on the `True Result` group and search for the `Get Quote` sub-action in the search bar.

    In the sub-action itself make sure you select `Random` as the `Type` and click `OK`. This will retrieve a random quote from the quotes.

    Next, we want to send the quote as a message. Add the sub-action `Twitch -> Chat -> Send Message to Channel` to the `True Result` group, and make sure it's under the `Get Random Quote` sub-action.
    In the  `Message` field you can write something like `%quoteId% %quote% - %quoteUser%` to send the quote ID, the quote itself and the user who added the quote.

5. Check whether input is a number or not

    In the `False` group of the If/Else block, we will continue down the path to retrieve a specific quote by its index.

    However first we want to check whether the input is a number or not, this would still be in the `False` group. 
    
    This can be done the following way:
    1. Add a sub-action Core -> Arguments -> Set Argument.
        - Variable Name: `quoteNum`
        - Value: `$math( floor( %input0% ) )$`

        The math function will round down the input to the nearest whole number. If the value of `input0` is not a number, the value of `quoteNum` will be `NaN` which we can check with another `if/else`.
        :read-more{to="/guide/variables#math"}

    2. Add another `If/Else` sub-action to check whether the `quoteNum` value is a number or not.
        - Input: `%quoteNum%`
        - Operation: `Equals`
        - Value: `NaN`

    In the `True` group, you can now add another sub-action to send a message to the channel that the input is not a number, or you simply leave it empty.

    In the `False` group, we will continue and try to retrieve the specific quote by its index.

    ![Counter Message](assets/quote-check-command-input.png)

6. Get a specific quote and send the message

    Since we have already checked that the input is a number, we can now retrieve the specific quote by its index.
    To do this we want to add the sub-action `Core -> Quotes -> Get Quote`, and as the `Type` we will select `Specific`. The `Quote ID` field will be set to `%quoteNum%`, which will retrieve the value of the `quoteNum` variable we set earlier.
    
    :read-more{to="/sub-actions/core/quotes/get-quote"}
    
    The last thing we want to do is check whether or not a quote was able to be retrieved. This can be done by adding yet another `If/Else` sub-action under the `Get Quote` sub-action.

    We want to check whether the argument `quote`, or other quote related arguments were even created by the `Get Quote` sub-action.
    - Input: `quote`
    - Operation: `Does Not Exist`

    Why do we not add % around `quote`? Because we don't want the value of the `quote` argument, but rather check if the literal name `quote` exists as an argument.
    
    - In the `True` group, we can add a sub-action to send a message to the channel that the quote was not found, or you can leave it empty.
    - In the `False` group, we can add the sub-action `Twitch -> Chat -> Send Message to Channel` to send the quote as a message.
        - For example: `#%quoteId%: %quote% - %quoteUser%`
    
    ![Counter Message](assets/quote-get-finished-action.png)

## Instructions (Add Quote)
  Adding a quote is fairly straightforward, we will create a new action that will be used to add a simple command input as the quote. This will it that the quote is referenced to the streamer, and not the the user who added it via the command.

1. Creating an action

    To create a new action head to the **Actions** tab and right-click in the actions section. Select **Add Action** and name it something like "Add Quote".

2. Adding the "!quoteadd" command trigger

    This step is pretty much the same as the previous one for just adding a !quote command. Just in this case we give it a different name and a different command itself.
    
    - Right-click in the **Triggers** section and select `Core -> Commands -> Command Triggered`.
    If you already have a command like "!quoteadd" and want to use that, you can select it from the dropdown menu. If not, you can create a new command by clicking on the `Create Command` button below the dropdown.

    Give the command a name like "Add Quote" and set the command itself to `!quoteadd`, or anything you like.
    Leave the location to `Start`, this will allow the command to also check an input.

    The other settings can be left as is, unless you want to change them. For example, you can set the `Cooldown` to prevent spamming the command.

3. Adding the quote itself

    Next, we want to add the quote itself. To do this, we will use the sub-action `Core -> Quotes -> Add Quote`.
    
    In the `Variable` field, we will write `%rawInput%`, this will get the whole input of the command, so the value of `rawInput`.

    ![Add Quote Sub-Action](assets/quote-add-quote-sub-action.png)

4. Check if the quote was added successfully

    After adding the quote, we want to check whether or not the quote was added successfully. This can be done by adding another `If/Else` sub-action.
    - Input: `%success%`
    - Operation: `Equals`
    - Value: `True`

    In the `False` group, we can then add a `Break` sub-action to stop the action from continuing, since the quote was not added successfully.
    
    Below the whole `If/Else` block, you can also put this in the `True` group`, we can then add a sub-action to send a message to the channel that the quote was added successfully.

    So create a sub-action `Twitch -> Chat -> Send Message to Channel` and write something like `Quote added successfully! ID: %quoteId% - %quote%` in the `Message` field.

## Import

As mentioned at the start here is the import for Streamer.bot v1.0.0 and above. This includes the `!quote` and `!quoteadd` commands, and the needed actions.

```bash [streamerbot-import]
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
```