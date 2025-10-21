---
title: OBS Raw
navigation.title: Raw
description: Send custom requests directly to the OBS WebSocket server
parameters:
- name: ObsConnection
  import: obs-studio/connection
csharpMethods:
  - ObsSendRaw
---

:read-more{to=/guide/broadcasters/obs-studio}

::tip{to="https://obs-raw.streamer.bot"}
You can use the [OBS Raw Generator](https://obs-raw.streamer.bot) to generate raw requests in Raw JSON or C# Code format
::

## Variables
Variables are generated based on the configured request

::warning
If you are debugging and wish to populate the resulting variables from a Raw request, you must use a [Test Trigger](/api/triggers/core/test).
<br>
The `Test` button within the Raw sub-action dialog will **only** send the OBS request and does not populate any variables on its own.
::