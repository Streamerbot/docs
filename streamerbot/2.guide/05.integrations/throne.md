---
title: Throne
description: Integrate Streamer.bot with your Throne account
navigation.icon: null
version: 1.0.5
icon: arcticons:throne
---

Receive [Throne](https://throne.com) event triggers in Streamer.bot via webhooks

::note{to=/guide/integrations/streamerbot}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::steps{level=3}

### Create a new Webhook

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
On the Streamer.bot Website, navigate to [User Settings > Webhooks](https://streamer.bot/user/integrations/webhooks)
:::

1. Create a new webhook and select `Throne` as the integration type
1. Enter a name for this webhook, e.g. `"My Throne Webhook"`
1. Ensure the `Enabled` toggle is active

### Obtain your Webhook URL

1. Click `Configure` on the newly created webhook
1. Copy the `Webhook URL` - _you will need this for the next step when configuring Throne!_

### Configure Throne Webhooks

:::navigate{to=https://throne.com/profile/integrations/webhook target="\_blank"}
On the Throne Website, navigate to **Account > Settings > Integrations > Webhooks**, or [click here](https://throne.com/profile/integrations/webhook)
:::

1.  Click `Add URL`
1.  Paste your `Throne Webhook URL` from Streamer.bot into the `URL` field
1.  Ensure the `Enable Webhooks` toggle is enabled
1.  Click `Save`

:::success
Throne events should now be available as triggers in Streamer.bot!
:::

::

## Usage

:read-more{to="/api/triggers/integrations/throne"}
