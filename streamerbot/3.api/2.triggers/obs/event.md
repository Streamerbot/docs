# OBS Event
OBS Studio event trigger.

This event triggers when a selected OBS event occurs.

::callout{icon=i-mdi-bookmark to="https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events" target=_blank rel=noopener}
Explore all supported [OBS Studio Events](https://github.com/obsproject/obs-websocket/blob/master/docs/generated/protocol.md#events) on their WebSocket protocol documentation
::

## Parameters
### `OBS`
Select the configured [OBS Studio Connection](/guide/broadcasters/obs-studio) to connect to.

### `Event`
Select an or any event to react on.

## Variables
The variables of this trigger are different depending on the `Event` parameter.