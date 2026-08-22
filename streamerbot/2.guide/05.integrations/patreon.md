---
title: Patreon
description: Integrate Streamer.bot with your Patreon account
navigation.icon: null
icon: i-simple-icons-patreon
version: 0.1.8
logo: https://streamer.bot/img/integrations/patreon.png
---

Receive [Patreon](https://www.patreon.com/) event triggers in Streamer.bot via webhooks

::note{to=/guide/integrations/streamerbot}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::steps{level=3}

### Create a new Webhook

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
On the Streamer.bot Website, navigate to [User Settings > Webhooks](https://streamer.bot/user/integrations/webhooks)
:::

1. Create a new webhook and select `Patreon` as the integration type
1. Enter a name for this webhook, e.g. `"Patreon Webhook"`
1. Ensure the `Enabled` toggle is active

### Obtain your Webhook URL

1. Click `Configure` on the newly created webhook
1. Copy the `Webhook URL` - _you will need this for the next step when configuring Patreon!_
1. Leave this page open for later - _you will need to return here to paste your Patreon secret_

### Configure Patreon Webhooks

:::navigate{to="https://www.patreon.com/portal/registration/register-webhooks" target=\_blank rel=noopener}
On the [Patreon Platform](https://www.patreon.com/portal/registration/register-webhooks) website, navigate to **Patreon Platform > Applications > My Webhooks**
:::

1. Paste your `Patreon Webhook URL` from Streamer.bot into the `Create a new webhook...` input
1. Click the `+` button
1. Enable the events you would like to receive
   - _**Do not** enable any of the *deprecated* `pledges:*` events_
1. Click on `Copy Secret` to obtain your verification token for the next step

### Add your Patreon Secret

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
Return to your newly created webhook on the [Streamer.bot Website](https://streamer.bot/user/integrations/webhooks)
:::

1.  Paste the secret token into the `Verify Secret` input
1.  Click `Save` to save your changes

:::success
Patreon will now forward webhooks to Streamer.bot!
:::
::

## Usage

:read-more{to="/api/triggers/integrations/patreon"}
