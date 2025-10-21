---
title: Heart Rate Pulse
description: Trigger for a HypeRate Heart Rate Pulse
version: 0.1.5
parameters:
  - name: Range
    import: common/range
variables:
  - name: heartRate
    type: number
    description: Last measured heart rate BPM (beats per minutes)
    value: 87
---

::warning
When HypeRate.io is broadcasting your heart rate, this event can fire once every second, so be sure whatever action you use runs fast enough so it won't cause a backlog in the action queue. It is also recommended that whatever action you are running to be placed in a blocking queue.
::