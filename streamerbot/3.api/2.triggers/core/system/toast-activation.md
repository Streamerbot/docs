---
title: Toast Activation
description: Trigger for a Toast Activation
version: 0.2.0
variables:
  - name: toast.id
    type: string
    description: The indentifier for the toast
    value: Toast-1
  - name: toast.title
    type: string
    description: The title of the toast
    value: My toast title
  - name: toast.message
    type: string
    description: The message of the toast
    value: My toast message
  - name: toast.attribution
    type: string
    description: The attribution of the toast
    value: My toast attribution
  - name: toast.iconPath
    type: string
    description: The icon path of the toast
  - name: toast.localIconPath
    type: string
    description: The local icon path of the toast
---

## Parameters
::field-group
  ::field{name="Toast Id" type=Text}
    Filter on a specific ID to seperate multiple toast notifications from each other

    - Leaving this blank is considered a catch-all and will trigger on **any** id
  ::
::