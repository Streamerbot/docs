---
title: Create Record Chapter
description: Creates a chapter marker in the OBS Recording
version: 0.2.5
parameters:
  - name: Connection
    import: obs-studio/connection
  - name: Chapter Name
    type: String
    required: true
    description: |
      Type the name for the Chapter (does accept `%variables%`)
    value: '%game% - Victory!'
variables:
  - name: success
    type: boolean
    description: Returns whether or not a chapter was successfully created
    value: true
csharpMethods:
  - ObsCreateRecordChapter
---

::danger
**Recording Format Requirement**
<br>
This sub-action requires the `Recording Format` setting be configured to `Hybrid MP4 [BETA](.mp4)` in OBS Studio.
<br>
This can be found by going to `Settings -> Output -> Select the 'Recording' Tab -> Recording Format`
::