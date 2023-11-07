---
title: Patreon
description: Integrate Streamer.bot with your Patreon account
navigation.icon: null
icon: mdi:patreon
version: 0.1.8
logo: https://streamer.bot/img/integrations/patreon.png
---

Receive [Patreon](https://www.patreon.com/) event triggers in Streamer.bot via webhooks

::callout{color=amber icon=i-mdi-alert}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::callout{icon=i-mdi-navigation to="https://streamer.bot/user/settings#patreon" target=_blank rel=noopener}
Navigate to **Streamer.bot User Settings > Webhook Integrations > Patreon** on the Streamer.bot website
::

1. Set `Patreon Connection` to `Enabled`
2. Copy your `Patreon Webhook URL`

::callout{icon=i-mdi-navigation to="https://www.patreon.com/portal/registration/register-webhooks" target=_blank rel=noopener}
Navigate to **Patreon Platform > Applications > My Webhooks** on the [Patreon Platform](https://www.patreon.com/portal/registration/register-webhooks) website
::

1. Paste your `Patreon Webhook URL` from Streamer.bot into the `Create a new webhook...` input
2. Click the <kbd>+</kbd> button
3. Enable the events you would like to receive
    - Do not enable any of the *deprecated* `pledges:*` events
4. Click on `Copy Secret` to obtain your verification token

::callout{icon=i-mdi-navigation to="https://streamer.bot/user/settings#patreon" target=_blank rel=noopener}
Return to **Streamer.bot User Settings > Webhook Integrations > Patreon** on the Streamer.bot website
::

1. Paste your patreon secret into the `Patreon Webhook Secret` input

## Usage
::callout{icon=i-mdi-bookmark color=green to=/api/triggers/integrations/patreon/follow-created}
Explore the [Patreon Triggers](/api/triggers/integrations/patreon/donation) API references
::