---
title: Ko-Fi
description: Integrate Streamer.bot with your Ko-Fi account
navigation.icon: null
icon: simple-icons:kofi
version: 0.1.8
logo: /img/icons/ko-fi.png
---

Receive [Ko-Fi](https://ko-fi.com){target=_blank} event triggers in Streamer.bot via webhooks

::callout{color=amber icon=i-mdi-alert}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::callout{icon=i-mdi-navigation to="https://streamer.bot/user/settings#kofi" target=_blank rel=noopener}
Navigate to **Streamer.bot User Settings > Webhook Integrations > Ko-Fi** on the Streamer.bot website
::

1. Set `Ko-Fi Connection` to `Enabled`
2. Copy your `Ko-Fi Webhook URL`

::callout{icon=i-mdi-navigation to="https://ko-fi.com/manage/webhooks?src=sidemenu" target=_blank rel=noopener}
Navigate to **Ko-Fi > Settings > API** on the Ko-Fi website
::

1. Paste your `Ko-Fi Webhook URL` from Streamer.bot into the `Webhook URL` input
2. Click on `Advanced` and copy your `Verification Token`

::callout{icon=i-mdi-navigation to="https://streamer.bot/user/settings#kofi" target=_blank rel=noopener}
Return to **Streamer.bot User Settings > Webhook Integrations > Ko-Fi** on the Streamer.bot website
::

1. Paste the `Verification Token` into the `Ko-Fi Verification Token` input

::callout{icon=i-mdi-lightbulb color=amber}
You can send test webhooks from the Ko-Fi API page
::

## Usage
::callout{icon=i-mdi-bookmark color=green to=/api/triggers/integrations/ko-fi/donation}
Explore the [Ko-Fi Triggers](/api/triggers/integrations/ko-fi/donation) API references
::