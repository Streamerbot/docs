---
title: Streamer.bot Chat
description: The latest updates and improvements for Streamer.bot Chat and Overlay
---

## 📅 September 2, 2026

#### ✨ What's New

- Added Twitch GIF support for chat and overlay
  - By default, GIF's are shown in the chat feed and collapsed in overlay (configurable in settings)
- Split platform settings into separate pages for Twitch, YouTube, and Kick exclusive settings
- Added per-event style overrides for all chat events
  - Default styles can be configured per-platform, and then granularly overidden per-event
  - Support for this feature in the overlay is planned for a future update
- Added ability to explicitly hide events from the chat feed and the event feed, respectively
- Added randomized event previews for all events in settings
- YouTube event support added for:
  - New Subscriber
  - Jewels Gifted
  - Membership Gifts
- Added the ability to toggle display of chat badges in both the chat feed and the overlay

#### 🛠️ Improvements & Updates

- Updated YouTube events for payload changes in v1.1.0-alpha
- YouTube ban and timeout events now properly remove associated messages from chat and overlay
- Improved handling of input queries when completing slash commands

#### 🐛 Fixes

- Updated parsing of YouTube emojis in legacy and current versions of Streamer.bot
- Fixed autocompletion when using the `/action` slash command
- Fixed broken ban/unban links in Kick user details modal

## 📅 August 26, 2026

#### ✨ What's New

- **7TV Overlay Emotes Support**
- Added `Animate Emotes` toggle in settings for disabling animated emotes
- Added `AVIF` and `WEBP` support for animated emotes when supported by browser and emote provider

#### 🛠️ Improvements & Updates

- Many performance related improvements behind the scenes
- Updated event rows to prefer platform color highlight by default
- Improved handling of emote spacing in chat messages
- Updated YouTube Super Chat styles to match highlighted event styles
- Improved default text shadow in `Chat Overlay` mode
- Pronouns badge will now properly scale with the configured font size
- Improved sizing and alignment of user avatars
- Moved default user avatar next to username. Preserved previous far-left avatar slot for Twitch Shared Chat source avatar

#### 🐛 Fixes

- Miscellaneous payload fixes for `Streamer.bot v1.1.0-alpha`
- Fixed quick action platform override not applying to `Kick`
- Fixed an issue preventing pronouns from loading in certain scenarios
- Twitch Announcement events in `Chat Overlay` will now properly wrap

## 📅 August 19, 2026

#### ✨ What's New

- **Local font family support**
- Added optional ability to override font family via text entry
- New `Chat Overlay` settings for toggling display of user avatars and pronouns

#### 🛠️ Improvements & Updates

- Added additional [data-attribute] properties for event row CSS targeting (to match previous chat row changes)
- Improvements to user avatar sizing and alignment across Twitch, YouTube, and Kick chat messages

#### 🐛 Fixes

- <kbd>Tab</kbd> key now properly selects items when autocompleting `@username`, `:emote`, or `!command`
- Collapsed global and user quick action items now properly execute their associated actions
- Fixed an issue where username aliases were not being properly resolved on Twitch chat messages

## 📅 August 12, 2026

#### ✨ What's New

- Major UI refactor, underlying library updates
- Initial **Twitch Shared Chat** support added, with broadcaster avatar displayed when active
- New settings layout with sidebar navigation
- Add new overlay `Message Layout` configuration option
  - `Inline`: Display messages inline with the username
  - `Stacked`: Display the username stacked above the message
  - `Block`: Display messages as a separate block to the right of the username
- Add new overlay `Message Style` configuration option
  - `Text`: Display messages as text and no background or outline
  - `Soft`: Display messages with a soft background
  - `Subtle`: Display messages with a soft background and outline
  - `Outlined`: Display messages with an outline
- Add additional `[data-attribute]` properties for chat element CSS targeting
- Add configuration option for displaying avatars in chat message rows
- Add support for Twitch and Kick avatars (YouTube previously supported)
- Add support for `YouTube Memberships Gifted` events
- Add `Chat Browser Dock` page to settings area

#### 🛠️ Improvements & Updates

- Improved virtual list performance and stability
- Updated sub-navigation layout for monitored YouTube broadcast selection
- Removed background from chat overlay, defaulting to transparent
  - No CSS overrides required in browser sources anymore
- Normalized chat message DOM structure across Twitch, YouTube, and Kick message.

#### 🐛 Fixes

- Handle an error in Kick Gift Sub events when recipients are missing from the event payload
- Prevent custom font from applying to quick action dropdowns
- Added a graceful fallback when emote or badge image URL fails to load

---

## 📅 August 5, 2026

#### 🐛 Fixes

- Updated chat overlay to properly preserve cleared history on full reload

---

## 📅 July 30, 2026

#### 🐛 Fixes

- Fixed an issue with First Words using the configured highlight color for First Message
- Updated First Words detection for Twitch and Kick chat messages

---

## 📅 May 1, 2026

#### 🛠️ Improvements & Updates

- Remove color lighten modification and use Twitch username colors directly
