---
title: Log
description: Send output to the Streamer.bot log files
parameters:
  - name: Log Level
    description: The log level to use for this message
    type: Select
    required: true
    default: Information
    options:
      - value: Information
        description: General information that will always be shown in the log file
      - value: Warning
        description: Information when you want to warn about something
      - value: Debug
        description: Information specifically for debugging purposes
      - value: Verbose
        description: Verbose information that will only be logged if the user has their log level on verbose
  - name: Message
    description: The message to log
    type: String
    required: true
---

::tip
You can use this sub-action for debugging your actions and seeing what is happening when they run!
::