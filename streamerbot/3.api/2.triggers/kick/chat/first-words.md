---
title: First Words
description: Trigger for a Kick First Words
variables:
  - name: firstMessage
    type: bool
    description: indicator whether the user's message was the first message **ever** in the channel
    value: True
commonVariables:
  - KickUser
  - KickChat
---


## Details
This triggers when someone sends their first message of the stream.

The exact reset time is set in `Platforms -> Kick -> First Words` and is `12h` by default. That means that Streamer.bot must have been closed for 12 hours in order to reset the First Words trigger.

::tip
If you want to reset the First Words trigger, you can do so by going to `Platforms -> Kick -> First Words` and clicking the `Reset` button. This will reset the First Words trigger and allow it to be triggered again.
::


## Parameters
::field-group
  ::field{name="User Name" type=Text}
    If you want to filter on a user name, you can enter a user name in this field
  ::
  ::field{name="Is UserId" type=Checkbox}
    Check this field if the text in the `User Name` field is a user id
  ::
::
