---
title: Ko-Fi
description: Integrate Streamer.bot with your Ko-Fi account
navigation.icon: null
icon: simple-icons:kofi
version: 0.1.8
logo: /img/icons/ko-fi.png
---

Receive [Ko-Fi](https://ko-fi.com){target=\_blank} event triggers in Streamer.bot via webhooks

::note{to=/guide/integrations/streamerbot}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::steps{level=3}

### Create a new Webhook

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
On the Streamer.bot Website, navigate to [User Settings > Webhooks](https://streamer.bot/user/integrations/webhooks)
:::

1. Create a new webhook and select `Ko-Fi` as the integration type
1. Enter a name for this webhook, e.g. `"Ko-Fi Webhook"`
1. Ensure the `Enabled` toggle is active

### Obtain your Webhook URL

1. Click `Configure` on the newly created webhook
1. Copy the `Webhook URL` - _you will need this for the next step when configuring Ko-Fi!_
1. Leave this page open for later - _you will need to return here to paste your Ko-Fi verification token_

### Configure Ko-Fi Webhooks

:::navigate{to="https://ko-fi.com/manage/webhooks?src=sidemenu" target=\_blank rel=noopener}
On the Ko-Fi website, navigate to **Settings > API**
:::

1. Paste your `Ko-Fi Webhook URL` from Streamer.bot into the `Webhook URL` input
1. Click `Update` to save your changes
1. Expand the `Advanced` section and **Copy** your `Verification Token`

### Add your Verification Token

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
Return to your newly created webhook on the [Streamer.bot Website](https://streamer.bot/user/integrations/webhooks)
:::

1. Paste the `Verification Token` into the `Verify Secret` input
1. Click `Save` to save your changes

:::success
Ko-Fi will now forward webhooks to Streamer.bot!
:::

::

## Usage

:read-more{to="/api/triggers/integrations/kofi"}

## Troubleshooting

:::tip
You can send test webhooks from the Ko-Fi API page
:::
