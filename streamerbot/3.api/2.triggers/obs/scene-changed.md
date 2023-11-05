# OBS Scene Changed
OBS Studio scene changed trigger.

This event triggers when a scene gets changed in OBS.

## Parameters
### `OBS`
Select the configured [OBS Studio Connection](/guide/broadcasters/obs-studio) to connect to.

### `Scene Name`
Here you can specify a scene name if you only want it to trigger this event when you switch to a specific scene. If you leave this field empty it will trigger on every scene.

## Variables
:variables-description

Name | Description
----:|:------------
`obs.id` | The connection id
`obs.name` | The name of the connection
`obs.host` | The IP Address of the OBS connection `default: 127.0.0.1`
`obs.studioVersion` | The current OBS Studio version
`obs.websocketVersion` | The current OBS websocket version
`obs.sceneName` |	The new scene name