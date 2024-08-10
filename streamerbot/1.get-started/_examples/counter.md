---
title: Creating a counter
description: Create a simple counter to count up or down
icon: i-mdi-numeric-positive-1
---

## Creating a counter

Counters can be used in various ways – for death counters in videogames, counting how many times the streamer has yawned or how many times a specific command has been used. While commands and Twitch channel point rewards offer their own inbuilt counters, they're not as versatile as the following method that is using **global variables**. If you want to know more about global variables, you can read about them [here](https://docs.streamer.bot/guide/variables#global-variables).

![Counter Preview](assets/example_counter_chat.png)

### 1. Creating a new action

First off, we create a new action and assign the trigger that we want to use for the counter to go up. In this example, we'll create a yawn counter and want it to add `+1` to the counter when a `!yawn` command has been used.

![Counter Action](assets/example_counter_action_1.png)

### 2. Creating the global variable

Now we create our actual global variable. This is done by the **Global (Set)**  subaction that we can find under `Core -> Globals -> Global (Set)`. We can give it any name we want and choose **Increment** in the dropdown menu, because we want to **add** a value. We can now type `1` in here to add 1 to the value each time we trigger the action. If we leave it empty, it will also default to 1.

![Counter Global Set Subaction](assets/example_counter_global_set.png)

### 3. Bring the global variable into the action

Global variables work a little different than regular variables that we use in our actions, because they don't just disappear into the void once the action has finished. So by default they're not available within the action (even after creating it in that very same action), unless we **call** them. For that we create a **Global (Get)** subaction to bring our newly created global variable from above as a regular variable into our action.

![Counter Global Get Subaction](assets/example_counter_global_get.png)

So `Variable Name` is the actual name of our global variable (the name in our **Global (Set)** subaction). In our case, it's `yawnCounter`. 

The `Destination Variable` is its new name that we can use as a variable in our action. It can have a different name like `yawnCounterVariable`, but for sake of simplicity we can just give it the same name. 

The `Default Value` assigns a value if the variable doesn't exist at the time we are calling it. But since we created it before with our **Global (Set)** subaction, this is technically redundant.

### 4. Using our new variable

We're pretty much done! Now each time we use our `!yawn` command, it will increment the `yawnCounter` global variable by `+1` and we can then for instance use that in a Twitch Message subaction:

`Streamer has yawned %yawnCounter% times already 🥱`

![Counter Message](assets/example_counter_message_1.png)

You can also create a second action and choose `Decrement` on the **Global (Set)** subaction instead to lower the counter with each trigger.

### 5. Done!

---

_Note: **Persisted** Global (Non-User) Variables have a special gimmick: they can be called into the action without the need of a **Global (Get)** subaction. For this, we can wrap the name of the global variable into waves instead of percent symbols. So instead of `%yawnCounter%`, we simply write `~yawnCounter~`. This only works for this specific kind of global variables. Non-persisted **and** global user variables will need a preceding **Global (Get)** subaction._

![Counter Variant 2](assets/example_counter_action_2.png)

![Counter Variant 2 Message](assets/example_counter_message_2.png)
