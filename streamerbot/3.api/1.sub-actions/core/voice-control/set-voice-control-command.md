---
title: Set Voice Control Command
description: Voice Control Sub-Actions Reference
published: true
date: 2023-04-10T05:43:28.412Z
tags: twitch, integrations, voice, youtube, streamerbot
editor: markdown
dateCreated: 2022-07-04T01:16:31.435Z
---

## Overview
With the Streamer.bot (0.18 +) you can now assign an action to a voice control command, then trigger this with a keyword or sentence that you say.
To do this you need to make sure you have streamer.bot listening to you on the correct input device. The microphone that you are going to use. 

### Pre-requirement 
First open streamer.bot and then navigate the following tabs `Voice Control` then in the second row of tabs click `Settings` in this take provide you have a support speech recognition package installed it should be usable.
You will want the bot to start listening to you when you start the bot up so go ahead and enable the "Auto Start Listen" by checking the box just like the image below. Also in this tab on the bottom is the "Audio Input Device"
when you have done this be sure the bot is listening by click the **Start Listening** button. click Save button at the top.

![vc-setting-tab.png](/voice-control/vc-setting-tab.png)

### Setting up your voice command 

First make sure that streamer.bot is open and then navigate through the following tabs `Voice Control` then in the second row of tabs click `Commands` in this tab is where we set up the voice commands so in the white space right click here and click `Add` a new dialog box will appear like the one below.

![vc-add-dialog.png](/voice-control/vc-add-dialog.png =400x)

In this dialog you can see the following option and input fields we need to configure so starting with the top input field 

**Name** - here you would need to enter the name of the voice command (This is how you would identify this later.)
**Enabled** - this check box controls whether the voice command is enabled or not.
**Command** - In this input field you need to type what you're going to say. (This is what streamer.bot will listen for before it runs the action that is attached)
**Location** - This drop down lets you choose from 3 options 
- <p style="text-align: center;">  Exact - what you say, needs to match whatever you have typed in Command Input field.
-  Start - the bot will listen for the command you've inputted in the command field at the beginning of the sentence ensure you have the `stop after` checked so the bot will pause listening for that command while the action its link to linked is running.
- Anywhere - the bot will trigger the command anywhere you say the text you inputted in the command field. Ensure you have the stop after checked so the bot will pause listening for that command while the action linked is running.</p>

**Action** - click the `<No Action Selected>` button to select the action you want to run when you say the command you entered in the command field.
**Override Global** -  only check this is you want the bot to trigger a command with specific certainty that you said the trigger words. this threshold is defined in the `Confidence Threshold` input field.

When you happy with this click the `Ok` button. Save then you have created your first of many voice control commands 

---

- [<i class="mdi mdi-chevron-left"></i> **Voice Control Sub-Actions Reference *Go Back***](/Sub-Actions/Voice-Control)
{.btn-grid .my-5}