---
description: Fetch all clips for the connected Twitch Broadcaster
parameters:
  - import: TwitchClipIsFeatured
---

::tip
Clip data is always sorted by view count (descending) due to Twitch API limitations
::

::warning
  A maximum of `1,000` clips can be returned
::