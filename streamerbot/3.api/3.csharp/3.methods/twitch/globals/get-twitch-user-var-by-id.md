---
name: GetTwitchUserVarById
title: GetTwitchUserVarById
description: Get the value of a user global variable for a specific Twitch user, by ID
parameters:
  - name: userId
    import: core/users/id
  - name: varName
    import: core/globals/name
  - name: persisted
    import: core/globals/persisted
---