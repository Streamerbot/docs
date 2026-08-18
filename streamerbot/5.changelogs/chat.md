---
title: Streamer.bot Chat
description: The latest updates and improvements for Streamer.bot Chat and Overlay
---

## 📅 August 12, 2026

#### ✨ What's New

- Major UI refactor, underlying library updates
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

#### 🐛 Fixes

- Handle an error in Kick Gift Sub events when recipients are missing from the event payload
- Prevent custom font from applying to quick action dropdowns

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
