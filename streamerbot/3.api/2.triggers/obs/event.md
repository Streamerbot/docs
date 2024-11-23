---
title: OBS Event
description: Trigger for an OBS Event
version: 0.2.0
parameters:
  - name: ObsConnection
  - name: Event
    type: Select
    required: true
    description: Select an event to Trigger on
variables:
  - name: obs.id
    type: string
    description: The connection id
  - name: obs.name
    type: string
    description: The name of the connection
    value: Main OBS
  - name: obs.host
    type: string
    description: The IP Address of the OBS connection
    value: 127.0.0.1
  - name: obsEvent.*
    type: string
    description: The properties of the OBS event, as flattened JSON keys.
---

::read-more{to="https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events"}
Explore all supported [OBS Studio Events](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events) on their WebSocket protocol documentation
::

::tip
The variables populated by this trigger are different depending on the `Event` parameter.
::

For example, given the following event data from OBS:

```json [example.json]
{
  event: "SceneListChanged",
  scenes: [
    {
      sceneIndex: 0,
      sceneName: "Be Right Back",
      sceneUuid: "1234-5678-9abcd"
    }
  ]
}
```

The following variables will be populated:

| Name | Type | Value |
| ---- | ---- | ----- |
| `obsEvent.event`{lang=cs} | `string` | `"SceneListChanged"`{lang=cs} |
| `obsEvent.scenes[0].sceneIndex`{lang=cs} | `int` | `0`{lang=cs} |
| `obsEvent.scenes[0].sceneName`{lang=cs} | `string` | `"Be Right Back"`{lang=cs} |
| `obsEvent.scenes[0].sceneUuid`{lang=cs} | `string` | `"1234-5678-9abcd"`{lang=cs} |