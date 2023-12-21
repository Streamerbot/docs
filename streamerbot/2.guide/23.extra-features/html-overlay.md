---
title: HTML Overlay
description: Overlay a custom browser source on your own screen!
logo: https://streamer.bot/logo-transparent.svg
---

## Introduction
This is a simple cross-platform app that runs in the background, allowing for a browser source to be displayed on the creator's desktop, creating an overlay on their own screen.

For example, the app comes preconfigured to show a simple dark splat that will cover most of the screen, (think Mario Kart oil spots) distracting them.

All you need to do is create a Channel Reward with the name ***SPLAT*** then relax and enjoy the distraction.

It also comes preconfigured to rain emotes down over the content on screen.

::callout{icon=i-mdi-warning color=amber}
This feature requires the **WebSocket Server** to be enabled in your Streamer.bot application
::

::callout{icon=i-mdi-heart color=pink}
Special thanks to **Ruirize** for the development.
::

## Download
Download the HTML Overlay application from and unzip the contents to your desired location.

::card-group
  ::card{icon=i-mdi-download title="HTML Overlay" to="https://cdn.streamer.bot/html-overlay/HTML%20Overlay%20v1.0.1.zip" target=_blank}
  `v1.0.1`
  <br>
  _Updated 2023-12-21_
  ::
::

::callout{icon=i-mdi-warning color=amber}
**Do not extract directly into your Streamer.bot folder.**<br>
Any outside location or a subdirectory within your Streamer.bot folder is fine.
::

## Usage

Open the extracted `HTML Overlay` directory and open `HTMLWindowsOverlay.exe` to start the application.

You will see a quick dark flash and then your desktop will return to normal.

::callout{icon=i-mdi-check color=green}
The HTML Overlay application is now running!
::

You should also now see an accompanying icon your system tray.

::callout{icon=i-mdi-lightbulb color=amber}
You can close HTML Overlay by :shortcut{value=Double-Clicking} the tray icon at any time.
::

### Configuration

::callout{icon=i-mdi-alert color=amber}
Your **Streamer.bot WebSocket Server** must be **enabled** for the application to interact with your bot
::

#### Streamer.bot Connection
By default, the HTML Overlay will attempt to connect to your Streamer.bot WebSocket Server using the default settings, `http://localhost:8080/`.

If you have changed the `host`, `port`, or `endpoint` values of your WebSocket server, you can configure this by modifying the `Content/index.html` file within the HTML Overlay directory.

## Modules
The HTML Overlay `zip` above is preloaded with 3 modules:

- Splat!
- Show Image
- Emote Rain

::callout{icon=i-mdi-lightbulb color=amber}
You can customize the options for each module by modifying the `Content/index.html` file
::

### Splat
Display a large paint splat on your screen.

#### Options
```js
{
  rewardTitle: "SPLAT". // Set your Twitch reward title you want to trigger this overlay
}
```

### Show Image
Display any image (from a URL) on your screen.

#### Options
```js
{
  rewardTitle: "Show Image", // Set your Twitch reward title you want to trigger this overlay
  imageUrl: "https://streamer.bot/logo.png". // Set to the image URL you want to display
  seconds: 5, // Number of seconds to display the image
  width: "auto", // Set a custom image width, accepts CSS values
  height: "auto", // Set a custom image height, accepts CSS values
}
```

### Emote Rain
Generate raining emotes from incoming Twitch chat messages.

#### Options
```js
{
  maxEmotes: 20, // Set to the max amount of emotes to accept from a single message
  emoteSize: "100px", // Set the size for the emote images on your screen
}