---
title: Version 0.0.30
description: 
published: true
date: 2023-06-11T18:26:03.060Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:35:07.602Z
---

* Misc fixes/improvements
* Fix issue related to OBS GDI Text source
{.changelog-fixes}

<span></span>

* Get list of categories on CPH launch, this data is cached and can be refreshed manually (used for event settings)
* Logic IF action has been updated to handle different data types, and included the > and < compairson operators, I still don't like how this is done, but, its a simple solution for now
{.changelog-updates}

<span></span>

* Add new event for broadcast update, both status and category
* Add/edit Channel Rewards directly within CPH
* Add new action to play a random sound from a folder
* Ability to choose audio output device application wide, and action specific (play sound + play sound from folder)
* Import/Export feature, you can import/export your actions and share them with others, or back them up
{.changelog-new}

## Channel Rewards
Can now manage the state of your Channel Rewards within CPH, toggle paused/enabled.

One caveat, CPH can not control rewards it has not created, this is a severe limitation of Twitch's API.  If you would like CPH to control a reward that is already created, you can use the duplicate ability to create a copy, the only thing that can not be copied or edited is the image associated with it, you'll have to edit this on the website.

There are new actions related to channel points, enabling/pausing, and mass enabling/pausing.

So on a category change, you could swap your rewards around.  If you've seen my dual streams with Lithaya, I use this to pause the redemption of the POV swapping rewards depending on which one was used.

Your current twitch authorization will be invalidated as 2 new scopes are required for channel reward management