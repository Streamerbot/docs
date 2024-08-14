---
title: Ko-Fi
description: Integrate Streamer.bot with your Ko-Fi account
navigation.icon: null
icon: simple-icons:kofi
version: 0.1.8
logo: /img/icons/ko-fi.png
---

Receive [Ko-Fi](https://ko-fi.com){target=_blank} event triggers in Streamer.bot via webhooks

::warning
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

1. Obtain your Ko-Fi Webhook URL
    ::navigate{to="https://streamer.bot/user/settings#kofi" target=_blank rel=noopener}
    Navigate to **User Settings > Webhook Integrations > Ko-Fi** on the Streamer.bot website
    ::

    1. Set `Ko-Fi Connection` to `Enabled`
    2. **Copy** your `Ko-Fi Webhook URL`

2. Configure Ko-Fi to send Webhooks

    ::navigate{to="https://ko-fi.com/manage/webhooks?src=sidemenu" target=_blank rel=noopener}
    Navigate to **Ko-Fi > Settings > API** on the Ko-Fi website
    ::

    1. Paste your `Ko-Fi Webhook URL` from Streamer.bot into the `Webhook URL` input
    2. Click on `Advanced` and **Copy** your `Verification Token`

3. Add your Verification Token

    ::navigate{to="https://streamer.bot/user/settings#kofi" target=_blank rel=noopener}
    Return to **User Settings > Webhook Integrations > Ko-Fi** on the Streamer.bot website
    ::

    1. Paste the `Verification Token` into the `Ko-Fi Verification Token` input

4. Done!

    Ko-Fi will now forward webhooks to Streamer.bot!

    ::tip
    You can send test webhooks from the Ko-Fi API page
    ::

## Usage
:api-reference-cards{path=integrations/ko-fi manifest-path=kofi}