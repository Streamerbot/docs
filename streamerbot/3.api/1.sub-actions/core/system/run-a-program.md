---
title: Run a Program
description: Execute an external program or script
parameters:
  - name: Command
    type: Text
    required: true
    description: |
      The command or executable to run

      This can contain anything you can normally execute via the :shortcut{value=Win+R} Windows Run dialog or `cmd`

      Examples:
      - Executables
        - `*.exe`
        - `node`
        - `python`
      - Batch Files
        - `*.bat`
      - PowerShell Scripts
        - `*.ps1`
      - URI
        - `https://google.com`
        - `streamdeck://plugins/message/<PLUGIN_UUID>/<MESSAGE>`
        - `liv-app://camera/set/<CAMERA#>`

  - name: Working Directory
    type: Text
    default: Command Directory
    description: The working directory for the executed command
  - name: Arguments
    type: Text
    description: |
      Optional arguments or flags to pass to the executable

      _Powerful with variables!_
  - name: Wait for Exit
    type: Number
    default: 0
    description: |
      Time to wait, in seconds, for the executable to complete.

      ::tip
      Set a wait time to enable the ability to populate [variables](#variables) with command output!
      ::
  - name: Environment Variables
    type: Table
    description: |
      Define any optional environment variables you would like to pass to the executable

      _Powerful with variables!_
variables:
  - name: outputCount
    type: int
    description: Number of lines in output
    value: 1
  - name: output#
    type: string
    description: |
      Each line of output, where output1 is line 1, output2 is line 2, and so on...
    value: Hello, world!
---

