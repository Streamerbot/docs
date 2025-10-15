---
name: Destination
type: Select
default: Global
required: true
---

Select the destination type for the global variable

- `Global` - Set a general global variable (non user variable)
- `User (redeemer)` - Set a user global for the current user who **activated** the action
- `User (target)` - Set a user global for the `targetUser`
    - Used in conjunction with the [Get User Info for Target](/api/sub-actions/twitch/user/get-user-info-for-target) sub-action