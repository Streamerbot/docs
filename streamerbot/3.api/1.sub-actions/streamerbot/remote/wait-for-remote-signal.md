---
title: Wait For Remote Signal
description: Wait for a remote signal from another Streamer.bot instance
version: 0.2.4
parameters:
  - name: Instance
    type: Selection
    required: true
    description: Select a specific instance or send it to any
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
    description: Time in milliseconds until the action times out. If left blank, it will default to 30000 ms. If no signal it being send over in that time, the subaction will abort.
variables:
  - name: signalTimeout
    type: Bool
    description: Indicator whether the subaction timed out or not
    value: True/False
  - name: hasResult
    type: Bool
    description: Indicator whether a result is included
    value: True/False
  - name: signalName
    type: String
    description: The signal's name
    value: Test Signal
  - name: instanceId
    type: String
    description: The instance ID
    value: dc01c234-567e-412b-ab5e-9a5a8385b85d
  - name: instanceName
    type: String
    description: The name of the instance
    value: SB Laptop
  - name: instanceVersion
    type: String
    description: The Streamer.bot version of the instance
    value: 0.2.4-alpha.18
  - name: instanceOs
    type: String
    description: The instance's operating system
    value: windows
csharpMethods: []
---
