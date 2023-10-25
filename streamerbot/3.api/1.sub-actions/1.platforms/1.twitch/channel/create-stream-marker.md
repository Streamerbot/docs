# Create Stream Marker
Trigger creation of a Stream Marker on Twitch
:image-preview

You can use this to signify an important event, or as a reminder for a point in the stream you'd like to review in your VOD at a later time.

::list{type=warning}
- Stream Markers are only available if you have VOD's enabled on your channel!
::

## Parameters
### `Description`
The description of the stream marker.
- Type: `String`

## Variables
:variables-description

| Name | Description | Example |
|-----:|:------------|:--------|
`broadcastUser` | The Twitch display name of the broadcaster account | `StreamerBotUser12`
`broadcastUserName` | The Twitch user name of the broadcaster account | `streamerbotuser12`
`broadcastUserId` | The Twitch user ID of the broadcaster account | `123456789`
`broadcastIsAffiliate` | Boolean value indicating if the broadcast account is a Twitch affiliate | `True/False`
`broadcastIsPartner` | Boolean value indicating if the broadcast account is a Twitch partner | `True/False`

## C# Usage
:csharp-method{name=CreateStreamMarker}