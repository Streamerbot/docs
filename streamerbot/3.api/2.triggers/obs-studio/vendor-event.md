---
title: Vendor Event
description: Trigger for a when a vendor event is sent by a 3rd party plugin in OBS
version: 0.2.4
parameters:
  - name: ObsConnection
  - name: Vendor
    type: String
    required: false
    description: Type the vendor name (from the plugin author) into the input box
  - name: Event
    type: String
    required: false
    description: Type the event name (from the plugin author) into the input box
variables:
  - name: obsVendorEvent.vendor
    type: string
    description: The vendor name, this is set by the author of the plugin
  - name: obsVendorEvent.event
    type: string
    description: The name of the vendor event, this is set by the author of the plugin
---
