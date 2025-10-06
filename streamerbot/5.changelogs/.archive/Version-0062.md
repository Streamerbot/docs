---
title: Version 0.0.62
description: 
published: true
date: 2022-02-14T20:26:34.849Z
tags: 
editor: markdown
dateCreated: 2022-02-14T20:26:31.278Z
---

This is primarily a bug fix release, visit [Streamer.bot 0.0.61](/Changelogs/Archives/Version-0061) to see all the shiny new features and updates that were included

Just a small fix

* Fix double clicking on commands
* Possible startup error fix
* Fix strange behaviour with new control used for grouping in actions/commands

> **NOTE**
> Windows Defender may give a false positive, I believe this is due to the inclusion of the Roslyn compilers which power the C# compiling capabilities. The fact they're there and there is code within the app to compile stuff itself I believe is what's causing the flagging, I'm not sure how to remedy this.
{.is-warning}