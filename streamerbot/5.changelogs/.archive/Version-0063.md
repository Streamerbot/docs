---
title: Version 0.0.63
description: 
published: true
date: 2022-11-11T17:00:09.909Z
tags: 
editor: markdown
dateCreated: 2022-02-14T20:28:13.485Z
---

Visit [Streamer.bot 0.0.61](/Changelogs/Archives/Version-0061) and [Streamer.bot 0.0.62](/Changelogs/Archives/Version-0061) to see all the shiny new features and updates.

* Misc fixes/etc that I've probably forgot
* Change what modules are merged
* Fix delete key not removing references properly in Execute C# Code sub-action
* Fix OBS/SLOBS visibility state not setting a default state, which could lead to a crash
* Commands became unusable after editing a command, woops
* Fix creating rewards not having action assigned if one was chosen
{.changelog-fixes}

<span></span>

* Log files have been moved to their own logs folder
* All settings and cache files are now in their own data folder
* Tweak finding references for Execute C# code
{.changelog-updates}

<span></span>

* Add top/bottom move otpions for moving sub-actions
* New app icon
* Added 2 new scopes, to create clips, and to manage your broadcast (update title, set game, etc)  The app will notify you that you'll need to re-auth
* Added new Action Added/Updated/Deleted events, mostly to better support StreamDeck plugin
{.changelog-new}

# StreamDeck
Was tinkering around with StreamDeck plugins and managed to get a basic one working, you can create a new button and give it an action.  My experience with writing these plugins is very limited, so this version may not advance very far, but hopefully a more advanced one may eventually takes its place.

[StreamDeck Streamer.bot](https://github.com/nate1280/streamdeck-Streamer.bot)

# Logs and Settings
When starting Streamer.bot without a logs or data folder, it will auto-create these folders, and move any existing logs and settings into this folder for you, and carry on like normal.

# EXE Changes
You'll notice that the archive is a bit large, and contains more files now.  I've decided to split all System/Microsoft libraries out of the merge and will now be alongside the application.  I'm hoping that this might reduce the number of false positives in anti-malware applications.

# Execute C# Code
Finding refs for Execute C# has been improved, and seems to do a better job at finding system related references, this is still an ongoing tweaking.

This also occurs during an import when a C# sub-action is found, it will re-find references for your local system and update them, there still may need to be manual finding of refs, and the import/export process will likely improve for these scenarios (i.e. including external libraries, and more)