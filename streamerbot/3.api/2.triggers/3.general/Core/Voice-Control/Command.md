---
title: Command
description: Voice Control Triggers Reference
published: true
date: 2023-03-18T01:22:01.381Z
tags: 
editor: markdown
dateCreated: 2023-03-14T22:34:14.348Z
---

## Overview
This triggers when a voice control command is successfully used.

For a detailed guide on how Voice Control works in Streamer.bot see [this page](/Voice-Control).

## Configuration
### Voice Control
Select any or a specific command from the Voice Control tab.

## Variables
Name | Description
----:|:------------
`spokenText` | The full spoken phrase detected, *including the trigger phrase*
`spokenTextConfidence` | Voice Recognition confidence raw value
`spokenTextConfidencePercent` | Confidence value as a percentage
`altPhraseText#` | The text of an alternative phrase
`altPhraseConfidence#` | The confidence of an alternative phrase
`altPhraseConfidencePercent#` | The percentage of the confidence from an alternative phrase
`spokenTextInput` | Detected spoken phrase with trigger command stripped <br> (Only works with `Start` based commands)
`spokenCommand` | Detected Trigger command
{.vars-table}

> Change the `#` to a number from 0 to the end of the alt phrases. So e.g. `%altPhraseText0%`, `%altPhraseText1%`, `%altPhraseText2%`
{.is-info}

---

- [<i class="mdi mdi-chevron-left"></i>**Voice Control Triggers Reference *Go Back***](/Triggers/Core/Voice-Control)
{.btn-grid .my-5}