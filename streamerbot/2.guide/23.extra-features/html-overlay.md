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

## Included Overlays
The HTML Overlay `zip` above is preloaded with 3 overloay modules:

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
```

## Custom Overlays
::callout{icon=i-mdi-alert color=amber}
Custom overlays are an **advanced** use case and require **JavaScript** expertise
::

To get started, create a new `js` file inside the `Content` directory.

::callout{icon=i-mdi-lightbulb color=amber}
The configured [Streamer.bot Client](https://streamerbot.github.io/client) instance is available at `window.client` for interacting with Streamer.bot via WebSocket and subscribing to events
::

Here we are using the source of the included `show-image.js` as an example:

```js [Content/my-module.js]
// Here we are defining default configuration options
// and then using window.getScriptConfig to fetch any user-modified values
const config = Object.assign({
  rewardTitle: 'Show Image',
  imageUrl: 'https://streamer.bot/logo.png',
  seconds: 5,
  width: 'auto',
  height: 'auto',
}, window.getScriptConfig(import.meta.url));

// Here we are subscribing to Twitch Channel Point Rewards
// and triggering our overlay when the configured title matches a redemption
window.client.on('Twitch.RewardRedemption', (message) => {
  if ((message.data.reward.title || message.data.title) === config.rewardTitle) {
    showImage();
  }
});
```

Import your new module at the bottom of `Content/index.html`, after any existing `<script>` tags

```html [Content/index.html]
<!-- Add this at the end, after any existing <script> tags! -->
<script type="module" src="my-module.js">
{
  rewardTitle: "Show Image" // Add your user config overrides here
}
</script>
```

::callout{icon=i-mdi-lightbulb color=amber}
Take a look at the existing modules in the `Content` directory for examples
::