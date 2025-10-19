---
name: GetTwitchUserVar
title: GetTwitchUserVar
description: Get the value of a user global variable for a specific Twitch user, by username
parameters:
  - name: userName
    import: core/username
  - name: varName
    import: core/globals/name
  - name: persisted
    import: core/globals/persisted
---