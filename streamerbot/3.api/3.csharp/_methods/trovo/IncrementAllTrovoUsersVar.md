---
description: Increments the value of a specific user global variable for all Trovo users
version: 0.2.4
parameters:
  - name: varName
    description: Name of the user variable
  - name: value
    description: Value of how much the user variables should be incremented by
  - name: persisted
    description: |
      - `true` - Persisted user variables will be affected
      - `false` - Non-persisted user variable will be affected
---