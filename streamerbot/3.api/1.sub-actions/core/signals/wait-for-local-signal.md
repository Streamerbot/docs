---
title: Wait for Local Signal
description: Wait for a signal within the local instance of Streamer.bot
version: 0.2.4
parameters:
  - name: Signal Name
    type: String
    required: true
    description: Name of the signal. The signal names have to match for "Send" and "Wait".
  - name: Overwrite Variables
    type: Checkbox
    required: false
    description: If both actions (the sending and receiving one) have the same variable, the sending one will overwrite the receiving one when checked.
  - name: Timeout
    type: Int
    required: false
    description: Time in milliseconds until the action times out. If left blank, or set to higher than 30000ms, it will default to 30000 ms. If no signal has been received in that time, the sub-action will abort.
variables:
  - name: signalTimeout
    type: boolean
    description: Indicator whether the subaction timed out or not
    value: True/False
  - name: hasResult
    type: boolean
    description: Indicator whether a result is included
    value: True/False
  - name: signalName
    type: string
    description: The signal's name
    value: Test Signal
csharpMethods: []
---

::warning
If the subaction times out, only the `signalTimeout` will be populated with a value of `True`
::
