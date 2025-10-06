---
name: IncrementOrCreateKickUsersVarById
title: IncrementOrCreateKickUsersVarById
description: Increments the values of Kick user variables for a list of user IDs. If the variable does not exist for a user, it will be created and set to the incremented value.
version: 1.0.0
parameters:
  - name: userIds
    description: |
      List of user IDs to increment the variable for. If a user ID does not exist, it will be ignored.
      Example: `["123456789", "987654321"]`
  - name: varName
    description: Name of the user variable
  - name: value
    description: Value of how much the user variables should be incremented by
  - name: persisted
    description: |
      - `true` - Persisted user variables will be affected
      - `false` - Non-persisted user variable will be affected
---