---
name: Destination
type: Select
default: Global
required: true
options:
  - value: Global
    description: Set a general global variable (non user variable)
  - value: User (redeemer)
    description: Set a user global for the user who **activated** the currently executing action
  - value: User (target)
    description: |
      Set a user global for the user found in the `targetUser` argument
      <br>
      Commonly used in conjunction with the [Get User Info for Target](/api/sub-actions/twitch/user/get-user-info-for-target) sub-action
---

Select the destination type for the global variable
