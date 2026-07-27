---
title: Fourthwall
description: Integrate Streamer.bot with your Fourthwall account
navigation.icon: null
version: 0.2.3
logo: /img/icons/fourthwall.png
---

Receive [Fourthwall](https://fourthwall.com) event triggers in Streamer.bot via webhooks

::note{to=/guide/integrations/streamerbot}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::steps{level=3}

### Create a new Webhook

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
On the Streamer.bot Website, navigate to [User Settings > Webhooks](https://streamer.bot/user/integrations/webhooks)
:::

1. Create a new webhook and select `Fourthwall` as the integration type
1. Enter a name for this webhook, e.g. `"Fourthwall Webhook"`
1. Ensure the `Enabled` toggle is active

### Obtain your Webhook URL

1. Click `Configure` on the newly created webhook
1. Copy the `Webhook URL` - _you will need this for the next step when configuring Fourthwall!_
1. Leave this page open for later - _you will need to return here to paste your Fourthwall secret token_

### Configure Fourthwall Webhooks

:::navigate
On the Fourthwall Website, navigate to **Account > Settings > For Developers**
<br>
:icon{name=i-mdi-chevron-right class="w-4 mr-1"} `https://<YOUR_SHOP_NAME>.fourthwall.com/admin/dashboard/settings/for-developers`
:::

1.  Click `Create webhook`
1.  Paste your `Fourthwall Webhook URL` from Streamer.bot into the `URL` field
1.  Select the events you want to receive
1.  Click `Save`
1.  You should now see a message:
    `"Webhooks will be signed with secret token so you can verify their integrity:"`

1.  **Copy the secret token for the next step**

### Add your Fourthwall Secret

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
Return to your newly created webhook on the [Streamer.bot Website](https://streamer.bot/user/integrations/webhooks)
:::

1.  Paste the secret token into the `Verify Secret` input
1.  Click `Save` to save your changes

:::success
Fourthwall events should now be available as triggers in Streamer.bot!
:::

::

## Usage

:read-more{to="/api/triggers/integrations/fourthwall"}
