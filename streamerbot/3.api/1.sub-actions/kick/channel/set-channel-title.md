---
title: Set Channel Title
description: Update the current title of your Kick channel
parameters:
  - name: Title
    type: Text
    description: Enter the new title for your stream
variables:
  - name: titleSuccess
    type: bool
    description: The status of the sub-action request
    value: True/False
csharpMethods:
  - KickSetTitle
---