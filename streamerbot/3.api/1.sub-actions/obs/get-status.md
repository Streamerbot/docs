# Get Status
Get your OBS Studio output status
:image-preview

## Parameters
:parameter{name=ObsConnection}

## Variables
| Name | Description | Example |
|-----:|:------------|:--------|
`obs.isConnected` | If the selected OBS connection is connected | `True`/`False`
`obs.isStreaming` | If the selected OBS connection is streaming | `True`/`False`
`obs.isRecording` | If the selected OBS connection is recording | `True`/`False`

## C# Usage
:csharp-method{name=ObsIsConnected}
:csharp-method{name=ObsIsStreaming}
:csharp-method{name=ObsIsRecording}