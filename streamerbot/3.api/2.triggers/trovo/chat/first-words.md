---
title: First Words
description: Trigger for first words
parameters:
  - name: User Name
    description: If you want to filter on a specific user you can fill in a username here. If you don't want to filter on a specific user leave this field empty.
    type: Text
  - name: Is UserId
    description: If you want to filter instead on a user ID, check this box.
    type: Toggle
variables: []
commonVariables:
  - TrovoBroadcaster
  - TrovoChat
  - TrovoUser
---

The Trovo first words trigger executes when someone places their first chat message in the last 12 hours.

To reset the first words or change the 12 hours go to `Platforms > Trovo > Settings`