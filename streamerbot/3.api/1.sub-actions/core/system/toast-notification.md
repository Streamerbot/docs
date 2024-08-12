---
title: Toast Notification
description: Display a custom Windows toast notification
parameters:
  - name: Toast Id
    type: Text
    required: false
    description: |
      An optional identifier that uniquely identifies this toast or group of toasts.

      If two notifications have the same id, they will be displayed underneath the same header in Action Center.
  - name: Title
    type: Text
    required: true
    description: The title for the notification
  - name: Text
    type: Text
    required: true
    description: The text content for the notification
  - name: Attribution
    type: Text
    required: false
    default: Streamer.bot
    description: The author of the notification
  - name: Icon Path
    type: Text
    default: <Streamer.bot Location>\streamer.bot.png
    description: Enter the path to an image file to override the default notification image
---

## Preview
![toast preview](assets/toast-preview.png)