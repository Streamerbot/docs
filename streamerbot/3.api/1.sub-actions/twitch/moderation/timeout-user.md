---
title: Timeout User
description: Timeout a user
version: 0.2.4
parameters:
  - name: User Login
    type: String
    required: true
    description: Can be a user name or a variable like `%userName%`
  - name: Duration
    type: Int
    required: true
    description: Timeout duration in seconds. `0` is a permanent ban.
  - name: Reason
    type: String
    required: false
    description: Reason for the timeout
variables:
  - name: timedOutUser
    type: string
    description: display name of the timed out user
    value: GenericUser
  - name: timedOutUserName
    type: string
    description: login name of the timed out user
    value: genericuser
  - name: timedOutUserId
    type: string
    description: ID of the timed out user
    value: 12345678
  - name: timedOutUserType
    type: string
    description: platform of the timed out user
    value: twitch
  - name: timeoutResult
    type: bool
    description: indicator whether the timeout has been successful or not
    value: True/False
csharpMethods:
  - TwitchTimeoutUser
---


::note
**Moderators**
<br>
Timing out a moderator will automatically reassign their moderator status once the timeout period ends. Editors will not receive their editior rights back.
<br><br>
This only applies to the subaction. 
<br><br>
The C# method does not reassign their moderator status. You'll need to implement your own logic in C# to handle this.
::

