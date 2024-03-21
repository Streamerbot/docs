---
title: Raw
description: Make custom calls to the OBS websocket server for even more control over your OBS Studio instance
csharpMethods:
  - ObsSendRaw
---

:read-more{to=/guide/broadcasters/obs-studio}

::tip{to="https://obs-raw.streamer.bot"}
You can use the [OBS Raw Generator](https://obs-raw.streamer.bot) to generate raw requests in JSON or CPH format
::

## Parameters
::field-group
  :parameter{name=ObsConnection}
::

## Variables
Variables are generated based on the configured request

::warning
You need to use a [Test Trigger](/api/triggers/core/test) if you want to send a raw command **and** populate variables in Streamer.bot. The `Test` button within the sub-action dialog will **only** send the OBS request.
::