---
title: Creating a counter
description: Create a simple counter to count up or down
icon: i-mdi-numeric-positive-1
---

## Creating a counter

Counters can be used in various ways – for death counters in videogames, counting how many times the streamer has yawned or how many times a specific command has been used. While commands and Twitch channel point rewards offer their own inbuilt counters, they're not as versatile as the following method that is using **global variables**. If you want to know more about them, you can read it [here](https://docs.streamer.bot/guide/variables#global-variables).

## Creating a new action

1. First off, we create a new action and assign the trigger that we want to use for the counter to go up. In this example, we'll create a yawn counter and want it to add `+1` to the counter when a `!yawn` command has been used.

2. Now we create our actual global variable. We add the **Global (Set)**  subaction that we can find under `Core -> Globals -> Global (Set)`. We can give it any name we went and choose **Increment** in the dropdown menu, because we want to **add** a value.
