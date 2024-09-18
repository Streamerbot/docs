---
name: Source
type: Select
default: Global
required: true
---

Select the source type for the global variable

- `Global` - Fetch any general global variable (non user variables)
- `User (redeemer)` - Fetch a user global for the current user who **activated** the action
- `User (target)` - Fetch a user global for the `targetUser`
    - Used in conjunction with the [Get User Info for Target](/api/sub-actions/twitch/user/get-user-info-for-target) sub-action