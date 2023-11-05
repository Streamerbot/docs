---
version: 0.1.11
---

# Set Color
Update the color and brightness of your lights with Lumia Stream
:image-preview

## Parameters

### `Colour`
Set the new color of your light(s) in `hex` format

### `Brightness`
Set the new brightness for your light(s)
::list{type=warning}
- An empty value will leave the brightness at its current level
::

### `Duration`
Enter a duration, in milliseconds, to maintain these settings
::list
- *Optional*
- After the duration, the selected light(s) will revert to their default settings
::

### `Transition`
Enter a time, in milliseconds, to transition from your current light properties to the new configuration

### `Skip Queue`
Skip the current Lumia Stream queue
::list
- You can view the queue in your Lumia Stream dashboard
::

### `Default`
Set your light(s) to their default settings from Lumia Stream
::list{type=warning}
- This will ignore any previous parameters
::

### `Light`
Select the lights you would like to update
::list{type=warning}
- If no lights are selected, **all lights will be updated**
::

## C# Usage
:csharp-method