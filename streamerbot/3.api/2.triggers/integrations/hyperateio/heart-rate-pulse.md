---
title: Heart Rate Pulse
description: Trigger for a HypeRate Heart Rate Pulse
version: 0.1.5
variables:
  - name: heartRate
    type: number
    description: The heart rate BPM
    value: 87
---

## Details
::callout{icon=i-mdi-alert color=amber}
When HypeRate.io is broadcasting your heart rate, this event can fire once every second, so be sure whatever action you use runs fast enough so it won't cause a backlog in the action queue. It is also recommended that whatever action you are running to be placed in a blocking queue.
::

## Parameters
::field-group
  ::field{name=Range type=Range}
    :range-description
  ::
::