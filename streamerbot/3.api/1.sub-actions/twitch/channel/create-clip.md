# Create Clip
Create a 30 second Twitch Clip
:image-preview

::callout{color=amber icon=i-mdi-lightbulb}
Due to Twitch API restrictions, the generated clip will always be 30 seconds long and will be titled to match your current stream title.
To make your own changes to the clip duration or title, you must manually edit the clip later.
::

## Variables
:variables-description

| Name | Description | Example |
|-----:|:------------|:--------|
`createClipSuccess` | Boolean result of the reques | `True/False`
`createClipId` | String identifier of the created clip
`createClipCreatedAt` | Timestamp of clip creation | `7/11/2022 3:01:53 AM`
`createClipUrl` | Full URL to the created clip

## C# Usage
:csharp-method{name=CreateClip}