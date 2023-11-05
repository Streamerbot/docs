---
title: Play Sound
description: Sounds Sub-Action Reference
published: true
date: 2022-10-18T00:25:40.355Z
tags: 
editor: markdown
dateCreated: 2021-11-02T04:23:33.090Z
---

## Overview
Play a sound file on your computer.

![sub-action-sounds-play-sound-001.png](/sub-action-sounds-play-sound-001.png =400x)

## Configuration
### Audio Device
Pick the audio device the sound should be played through.

Application default will use whatever audio device is configured in the application settings.

### Sound file to play
The sound file you would like to play.  Supported audio formats are, `mp3`, `wav`, `m4a` and `ogg`

### Finish playing before continuing
Enabling this will wait for the duration of the sound file before continuing onto the next action.  If this is disabled, the sound will start being played and immediately carry onto the next sub-action.

### Volume
Adjust the volume of the sound file.  This is a very basic volume adjustment, and is usually better to adjust the volume with a tool like Audacity.