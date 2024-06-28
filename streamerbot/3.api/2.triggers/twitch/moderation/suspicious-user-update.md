---
title: Suspicious User Update
description: Trigger for when a Twitch user's restriction or monitor mode updates.
version: 0.2.4
variables:
  - name: moderator.userName
    type: string
    description: display name of the moderator who did the warning
    value: Lyfesaver74
  - name: moderator.login
    type: string
    description: login name of the moderator who did the warning
    value: lyfesaver74
  - name: moderator.id
    type: string
    description: display name of the moderator who did the warning
    value: 161545467
  - name: lowTrustStatus
    type: string
    description: the current mode
    value: restricted, active_monitoring, no_treatment
  
commonVariables:
  - TwitchUser
---
