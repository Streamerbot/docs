# OBS Recording Started
OBS Studio recording started trigger.

This event triggers when you start a recording in OBS.

## Parameters
### `OBS`
Select the configured [OBS Studio Connection](/guide/broadcasters/obs-studio) to connect to.

## Variables
:variables-description

Name | Description
----:|:------------
`obs.id` | The connection id
`obs.name` | The name of the connection
`obs.host` | The IP Address of the OBS connection `default: 127.0.0.1`
`obs.studioVersion` | The current OBS Studio version
`obs.websocketVersion` | The current OBS websocket version