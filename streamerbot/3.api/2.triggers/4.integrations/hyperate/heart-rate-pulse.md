# Heart Rate Pulse
HypeRate.io heart rate pulse trigger.

## Details
This event triggers every second while using a heart rate monitor.

::callout{icon=i-mdi-alert color=amber}
When HypeRate.io is broadcasting your heart rate, this event can fire once every second, so be sure whatever action you use runs fast enough so it won't cause a backlog in an action queue.  It is also recommended that whatever action you are running be placed in a blocking queue.
::

## Parameters
### `Range`
:range-description

## Variables
:variables-description

Name | Description
----:|:------------
`heartRate` | The heart rate BPM