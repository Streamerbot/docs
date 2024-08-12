---
title: Timed Actions
description: Trigger for a Timed Action
parameters:
  - name: Timers
    type: Select
    required: true
    description: |
      Select a timer from the Settings -> Timed Actions tab.

      ::tip
      You can quickly register a new timed action by clicking the `Create Timer` button!
      ::
variables:
  - name: timerId
    type: string
    description: The ID of the timer
    value: 4ed37eec-3b4d-49a5-ac63-57ae62f5231b
    version: 0.2.4
  - name: timerName
    type: string
    description: The name of the timer
    value: Socials
    version: 0.2.4
  - name: counter
    type: int
    description: A counter that tracks how many times the timer has fired (even if it’s not set to trigger any action, as long it's enabled)
    value: 5251
---

:read-more{to="/guide/settings/timed-actions"}
