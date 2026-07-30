---
title: Process Stopped
description: Trigger for when a Process is Stopped
version: 0.2.0
parameters:
  - name: Name
    type: Text
    description: |
      The name of the process to watch for. This is the name of the process as it appears in Task Manager.
      <br>
      An empty value is considered a catch-all and will trigger on **any** process started on your machine.
variables:
  - name: name
    type: string
    description: Name of the process watched for.
  - name: executable
    type: string
    description: Name of the process executable.
  - name: path
    type: string
    description: Path to the directory of the process.
  - name: fullPath
    type: string
    description: Exact path of the process executable.
  - name: processId
    type: string
    description: ID used in Windows for the process.
  - name: parentProcessId
    type: string
    description: ID of the program that launched the process.
---

::warning
**This trigger relies on the Process Watcher service**
<br>
You can enable the **Process Watcher** in Streamer.bot by navigating to `Services -> Process Watcher`
::
