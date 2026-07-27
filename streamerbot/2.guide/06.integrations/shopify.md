---
title: Shopify
description: Integrate Streamer.bot with your Shopify account
navigation.icon: null
icon: mdi:shopify
version: 0.1.14
logo: https://streamer.bot/img/integrations/shopify.svg
---

Receive [Shopify](https://shopify.com){target=\_blank} event triggers in Streamer.bot via webhooks

::note
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::steps{level=3}

### Create a new Webhook

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
On the Streamer.bot Website, navigate to [User Settings > Webhooks](https://streamer.bot/user/integrations/webhooks)
:::

1. Create a new webhook and select `Shopify` as the integration type
1. Enter a name for this webhook, e.g. `"Shopify Webhook"`
1. Ensure the `Enabled` toggle is active

### Obtain your Webhook URL

1. Click `Configure` on the newly created webhook
1. Copy the `Webhook URL` - _you will need this for the next step when configuring Shopify!_
1. Leave this page open for later - _you will need to return here to paste your Shopify verification token_

### Configure Shopify Webhooks

:::navigate
On the Shopify website, navigate to **Store Admin > Settings > Notifications**<br>
:icon{name=i-mdi-chevron-right class="w-4 mr-1"} e.g. `https://admin.shopify.com/store/YOUR_STORE_NAME/settings/notifications`
:::

1. Scroll to the bottom of the page and click `Create Webhook`
1. Set `Event` to `Order creation` or `Order payment`
   - You can create multiple webhooks if you would like to receive both events
1. Leave `Format` as `JSON`
1. Paste your `Shopify Webhook URL` from Streamer.bot into the `URL` field
1. Set the `Webhook API Version` to `Latest`
1. Click `Save`
1. You should now see a verification token highlighted in yellow - **copy this token for the next step**

### Add your Verification Token

:::navigate{to="https://streamer.bot/user/integrations/webhooks" target=\_blank rel=noopener}
Return to your newly created webhook on the [Streamer.bot Website](https://streamer.bot/user/integrations/webhooks)
:::

1. Paste the `Verification Token` into the `Verify Secret` input
1. Click `Save` to save your changes

:::success
Shopify will now forward webhooks to Streamer.bot!
:::

::

## Usage

:api-reference-cards{path=integrations/shopify}
