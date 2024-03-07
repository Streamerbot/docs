---
title: Set Color
description: Update the color and brightness of your lights with Lumia Stream
version: 0.1.11
parameters:
  - name: Colour
    type: Text
    required: true
    value: '#FFFFFF'
    description: |
      Set the new color of your lights in `hex` format

      ::tip
      You can open a color picker dialog by clicking the `...` button
      ::
  - name: Brightness
    type: Number
    required: false
    defautl: 100
    description: |
      Set a new brightness level for your lights

      An empty value will leave the brightness at its current level
  - name: Duration
    type: Number
    required: false
    default: 0
    description: |
      Optionally enter a duration, in milliseconds, to maintain these settings.

      The selected lights will revert to their default settings after the provided duration.
  - name: Transition
    type: Number
    required: false
    default: 1000
    description: Enter a time, in milliseconds, to transition from the current light properties to the new configuration
  - name: Skip Queue
    type: Toggle
    description: |
      Skip the current Lumia Stream queue and run this action immediately

      ::tip
      You can view the current queue in your Lumia Stream dashboard
      ::
  - name: Default
    type: Toggle
    description: |
      Set your lights to their default settings from Lumia Stream

      ::warning
      This will **override** any other configured parameters
      ::
  - name: Light
    type: Multi-Select
    description: |
      Select the lights you would like to update

      If no lights are selected, **all lights will be updated**
csharpMethods: []
---
