---
title: Heart Rate Pulse
description: Trigger for a Pulsoid Heart Rate Pulse
version: 0.1.5
parameters:
  - name: Range
    import: common/range
variables:
  - name: measuredAt
    type: number
    description: The epoch time from the measurement
    value: 1704063600
  - name: heartRate
    type: number
    description: Last measured heart rate BPM (beats per minute)
    value: 87
---

::warning
When Pulsoid is broadcasting your heart rate, this event can fire once every second, so be sure whatever action you use runs fast enough so it won't cause a backlog in the action queue. It is also recommended that whatever action you are running to be placed in a blocking queue.
::
