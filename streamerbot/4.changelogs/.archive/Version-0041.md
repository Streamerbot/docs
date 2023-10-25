---
title: Version 0.0.41
description: 
published: true
date: 2023-06-11T18:17:18.980Z
tags: 
editor: markdown
dateCreated: 2021-08-25T21:35:47.925Z
---

* Misc fixes/tweaks
* Fix Twitch authentication issues, it now forgets authentication, so you can re-auth to Twitch
* Fix OBS raw sub-action
* Fix startup to be a bit more reliable
{.changelog-fixes}

<span></span>

* Improvements to Twitch libraries (chat client and pub sub, how messages are handled)
* Improvements to OBS library, using new parsing code, seeing much lower CPU usage
* Change OBS Stop Streaming sub-action to OBS Streaming action to be able to Start/Stop streaming
* Update user list and information to a new style
* Update audio device selection
* Update data in events surrounding channel redemptions
{.changelog-updates}

<span></span>

* Add duration and days left to community goal contribution arguments (`%duration%`, `%daysLeft%`)
* Add decimal value of percentage to hype train events and community goals (`%percentDecimal%`)
* Add ability to change the volume level of playback, both at app level and in the `Play Sound`, and `Play Sound from Folder` sub-actions
* Auto-backup settings on startup
* Add global variables, and user global variables
* Add new sub-actions to support the global variables
* Add Websocket Server
* Add Websocket Client support
* Add UDP Listener
* Add Speech to Text capabilities
* Add Execute Code feature for inline C# code compilation
* Add new sub-action to set a channel redemption to cancelled (refund points), or fulfilled
* Add possible raiders names to the raid event as `%raiderNames%`
{.changelog-new}

## Auto Backup
Anytime CPH starts, it will now backup your configuration files before anything else is done, and place them in a time stamped backup zip, within a backup folder.

## Speech to Text
I've included basic Speech to text support within CPH, you can setup commands, which are specific words of phrases that can be detected, or you can use dictation for just talking and setup actions against words that may occur.

As this uses the built in Windows Speech Recognition engine, be sure you have trained this within Windows to get better results.

You can also change which input device is used for speech recognition.

## Execute Code
See [Execute Code](/Sub-Actions/Execute-Code) for full details and usage of this new sub-action

## Websocket Server
See [Websocket Server](/Servers-Clients/WebSocket-Server) for full details and usage of this new capability

## Websocket Client
See [Websocket Clients](/Servers-Clients/WebSocket-Clients) for full details and usage of this new capability

## UDP Listener
Using a port of your choice, you can send a UDP packet to execute an action you have available.  The settings for this are available through the `Websockets` tab.

```json
{
  "request": "DoAction",
  "action": {
    "id": "id (optional)",
    "name": "name (optional)",
  },
  "args": {
    "value": "value",
  }
}
```

If you are looking to add the ability to send a UDP packet within a program you are writing the following code is all that is needed to broadcast:

```csharp
public async Task SendUdpPacket(string udpMessage)
{
    var ipEndPoint = new IPEndPoint(IPAddress.Broadcast, Port);

    using (var udpClient = new UdpClient { EnableBroadcast = true })
    {
        var udpMessage = DynamicText.Parse(Payload, optional);

        var udpPayload = Encoding.UTF8.GetBytes(udpMessage);

        await udpClient.SendAsync(udpPayload, udpPayload.Length, ipEndPoint);
    }
}
```