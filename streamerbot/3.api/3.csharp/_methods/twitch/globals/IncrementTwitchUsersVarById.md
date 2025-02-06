---
description: | 
  Increments the values of Twitch user variables for a list of user IDs.
  Will only increment if variable exists
version: 0.2.4
parameters:
  - name: userIds
    descriptions: A List<string> of the user ids you want to increment the variables of
  - name: varName
    description: Name of the user variable
  - name: value
    description: Value of how much the user variables should be increased by
  - name: persisted
    description: |
      - `true` - Persisted user variables will be affected
      - `false` - Non-persisted user variable will be affected
---