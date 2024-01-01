---
title: First Words
description: Trigger for a Twitch First Words
version: 0.0.32
twitchService: Chat Client
variables: []
commonVariables:
  - TwitchUser
  - TwitchChat
---


## Details
This triggers when someone sends their first message of the stream.

## Parameters
::field-group
  ::field{name="User Name" type=Text}
    If you want to filter on a user name, you can enter a user name in this field
  ::
  ::field{name="Is UserId" type=Checkbox}
    Check this field if the text in the `User Name` field is a user id
  ::
::