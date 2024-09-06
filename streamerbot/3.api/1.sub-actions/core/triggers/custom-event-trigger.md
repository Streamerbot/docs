---
title: Trigger Custom Event
description: Triggers custom code events outside of C#
version: 0.2.5
parameters:
  - name: Event Name
    type: Text
    required: true
    description: Type the name of the custom code event to trigger
  - name: Use Args
    type: Toggle
    default: false
    description: Enable this option to enable parsing and replacement of `%variables%`{lang=cs} found within the Custom Event
---
