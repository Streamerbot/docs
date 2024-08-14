---
title: Patreon
description: Integrate Streamer.bot with your Patreon account
navigation.icon: null
icon: i-simple-icons-patreon
version: 0.1.8
logo: https://streamer.bot/img/integrations/patreon.png
---

Receive [Patreon](https://www.patreon.com/) event triggers in Streamer.bot via webhooks

::warning
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

1. Obtain your Patreon Webhook URL
    ::navigate{to="https://streamer.bot/user/settings#patreon" target=_blank rel=noopener}
    Navigate to **User Settings > Webhook Integrations > Patreon** on the Streamer.bot website
    ::

    1. Set `Patreon Connection` to `Enabled`
    2. Copy your `Patreon Webhook URL`

2. Configure Patreon to send Webhooks
    ::navigate{to="https://www.patreon.com/portal/registration/register-webhooks" target=_blank rel=noopener}
    Navigate to **Patreon Platform > Applications > My Webhooks** on the [Patreon Platform](https://www.patreon.com/portal/registration/register-webhooks) website
    ::

    1. Paste your `Patreon Webhook URL` from Streamer.bot into the `Create a new webhook...` input
    2. Click the <kbd>+</kbd> button
    3. Enable the events you would like to receive
        - _**Do not** enable any of the *deprecated* `pledges:*` events_
    4. Click on `Copy Secret` to obtain your verification token

3. Add your Webhook Secret
    ::navigate{to="https://streamer.bot/user/settings#patreon" target=_blank rel=noopener}
    Return to **User Settings > Webhook Integrations > Patreon** on the Streamer.bot website
    ::

    1. Paste your patreon secret into the `Patreon Webhook Secret` input

4. Done!
    ::success
    Patreon will now forward webhooks to Streamer.bot!
    ::

## Usage
:api-reference-cards{path=integrations/patreon}