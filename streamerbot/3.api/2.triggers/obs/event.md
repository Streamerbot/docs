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

## Notes
The variables populated by this trigger are different depending on the `Event` parameter.  For example, if the event data is:
```json
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
then the event variables will be:
- `obsEvent.event` : `SceneListChanged`
- `obsEvent.scenes[0].sceneIndex` : `0`
- `obsEvent.scenes[0].sceneName` : `Be Right Back`
- `obsEvent.scenes[0].sceneUuid` : `1234-5678-9abcd`


::bookmark{to="https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events"}
Explore all supported [OBS Studio Events](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events) on their WebSocket protocol documentation
::