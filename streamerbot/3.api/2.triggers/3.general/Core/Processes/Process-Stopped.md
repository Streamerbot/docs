# Process Stopped

Process Stopped trigger.

## Details

This event triggers when a process is stopped.

## Parameters

### `Name`

Input the name of the process to watch for.

::callout{icon=i-mdi-lightbulb color=amber}
Leaving this blank is considered a catch-all and will trigger on ANY process stopped.
::

## Variables

:variables-description

Name | Description
----:|:------------
`name` | Name of the process watched for.
`executable` | Name of the process executable.
`path` | Path to the directory of the process.
`fullPath` | Exact path of the process executable.
`processId` | ID used in Windows for the process.
`parentProcessId` | ID of the program that launched the process.
