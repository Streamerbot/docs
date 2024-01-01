---
title: Process Stopped
description: Trigger for when a Process is Stopped
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

## Parameters
::field-group
  ::field{name=Name type=Text}
    Input the name of the process

    - Leaving this blank is considered a catch-all and will trigger on **any** process started
  ::
::