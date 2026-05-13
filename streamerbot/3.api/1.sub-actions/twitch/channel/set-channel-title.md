---
title: Set Channel Title
description: Update the current title of your Twitch channel
parameters:
  - name: Title
    type: Text
    description: Enter the new title for your stream
variables:
  - name: titleSuccess
    type: bool
    description: Whether or not the channel title was successfully changed
    value: true/false
    
csharpMethods:
  - SetChannelTitle
---
