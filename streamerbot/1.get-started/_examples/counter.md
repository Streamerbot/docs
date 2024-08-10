---
title: Creating a counter
description: Create a simple counter to count up or down
icon: i-mdi-numeric-positive-1
---

## Creating a counter

Counters can be used in various ways – for death counters in videogames, counting how many times the streamer has yawned or how many times a specific command has been used. While commands and Twitch channel point rewards offer their own inbuilt counters, they're not as versatile as the following method that is using **global variables**. If you want to know more about global variables, you can read about them [here](https://docs.streamer.bot/guide/variables#global-variables).

## Creating a new action

1. First off, we create a new action and assign the trigger that we want to use for the counter to go up. In this example, we'll create a yawn counter and want it to add `+1` to the counter when a `!yawn` command has been used.

2. Now we create our actual global variable. This is done by the **Global (Set)**  subaction that we can find under `Core -> Globals -> Global (Set)`. We can give it any name we want and choose **Increment** in the dropdown menu, because we want to **add** a value. We can now type `1` in here to add 1 to the value each time we trigger the action. If we leave it empty, it will also default to 1.

3. Global variables work a little different than regular variables that we use in our actions, because they don't just disappear into the void once the action has finished. So by default they're not available within the action, unless we **call** them. For that we create a **Global (Get)** subaction to bring our newly created global variable from the first subaction as a regular variable into our action.

   So the `Variable Name` is the actual name of our global variable (the name in our **Global (Set)** subaction) and the `Destination Variable` is its new name that we can use as a variable in our action. It can have a different name, but for sake of simplicity we can just give it the same name. The `Default Value` assign a value if the variable doesn't exist at the time we are calling it. But since we created it before, this is technically redundant.

4. We're pretty much done! Now each time we use our `!yawn` command, it will increment the `yawnCounter` global variable by `+1` and we can then for instance use that in a Twitch Message subaction!

   `Streamer has yawned %yawnCounter% times already`


Note: **Persisted** Global (Non-User) Variables have a special gimmick: they can be called into the action without the need of a **Global (Get)** subaction. For this, we can wrap the name of the global variable into waves instead of percent symbols. So instead of `%yawnCounter%`, we simply write `~yawnCounter~`. This only works for this specific kind of global variables. Non-persisted **and** global user variables will need a preceding Global (Get) subaction.
