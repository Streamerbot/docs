---
title: User Global Variable Updated
description: Triggered when a user global variable has been updated
version: 0.2.3
parameters:
  - name: Variable Name
    type: Text
    description: |
      Enter the name of a specific user global variable

      Leave empty to trigger on **any** user global variable.
  - name: Persisted
    type: Select
    required: true
    default: Either
    description: |
      - `Either` - Trigger on **both** persisted and non-persisted variables
      - `Yes` - Trigger only on **persisted** variables
      - `No` - Trigger only on **non-persisted** variables
  - name: User Login
    type: Text
    description: |
      Enter the username of a specific user

      Leave empty to trigger on **any** username
  - name: Platform
    type: Select
    description: |
      - `Any` - Trigger on variable updates for **all** platforms
      - `Trovo` - Only trigger on **Trovo** user variable updates
      - `Twitch` - Only trigger on **Twitch** user variable updates
      - `VStream` - Only trigger on **VStream** user variable updates
      - `YouTube` - Only trigger on **YouTube** user variable updates
variables:
  - name: global.name
    type: string
    description: The name of the global variable
    value: myGlobalVariable
  - name: global.newValue
    type: string
    description: The new value of the global variable
    value: My new value
  - name: global.oldValue
    type: string
    description: The previous value of the global variable
    value: My old value
  - name: global.persisted
    type: bool
    description: Is this global variable persisted?
    value: True
  - name: global.lastWrite
    type: DateTime
    description: The timestamp of the last write
    value: 8/4/2023 10:56:06 AM
  - name: global.userId
    type: string
    description: The unique platform ID of the user
    value: '123456789'
  - name: global.userType
    type: string
    description: |
      The platform of the user: <br>
      `twitch`, `youtube`, `trovo`, `vstream`
    value: 'twitch'
  - name: global.userLogin
    type: string
    description: The username of the user
    value: cooluser420
  - name: global.userName
    type: string
    description: The disply name of the user
    value: CoolUser420
---