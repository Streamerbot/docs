---
title: Present Viewers
description: Trigger for YouTube viewer changes
variables:
  - name: users
    description: All the viewers in your stream <br> <small>Can only be accessed in C#</small>
  - name: isLive
    type: bool
    description: Your current streaming status
    value: true
  - name: title
    type: string
    description: The title of your stream
commonVariables:
  - YouTubeBroadcaster
---