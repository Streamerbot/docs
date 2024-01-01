---
title: Subscription
description: Trigger for a Twitch Subscription
twitchService: Chat Client
variables:
  - name: tier
    type: string
    description: The subscription tier<br>`prime`, `tier 1`, `tier 2`, `tier 3
    value: tier 1
commonVariables:
  - TwitchUser
  - TwitchChat
---

## Parameters
::field-group
  ::field{name=Tier type=Checkbox}
    Choose on which tier to trigger the subscription
    - Options:
      - Prime
      - Tier 1
      - Tier 2
      - Tier 3
  ::
::