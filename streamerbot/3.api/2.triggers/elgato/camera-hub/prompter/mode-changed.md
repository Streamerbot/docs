---
title: Mode Changed
description: When the mode of the Elgato Prompter has changed
variables:
  - name: mode
    type: number
    description: |
      The mode that has been selected, possible values are

      - 1 - Text Mode
      - 2 - Chat (Beta) Mode
      - 3 - Display Mode
  - name: modeString
    type: string
    description: |
      The friendly name for the mode the Elgato Prompter is in

      - 'Text' - This is the default mode, and displays the chapters that are setup in CameraHub
      - 'Chat (Beta)' - This is CameraHub's integrated Twitch Chat display
      - 'Display' - This makes the prompter act as a monitor, extending your desktop
  - name: oldMode
    type: string
    description: |
      The previous mode that was selected
---
