---
title: Shopify
description: Integrate Streamer.bot with your Shopify account
navigation.icon: null
icon: mdi:shopify
version: 0.1.14
logo: https://streamer.bot/img/integrations/shopify.svg
---

Receive [Shopify](https://shopify.com){target=_blank} event triggers in Streamer.bot via webhooks

::callout{color=amber icon=i-mdi-alert}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::callout{icon=i-mdi-navigation to="https://streamer.bot/user/settings#shopify" target=_blank rel=noopener}
Navigate to **Streamer.bot User Settings > Webhook Integrations > Shopify** on the Streamer.bot website
::

1. Set `Shopify Connection` to `Enabled`
2. Copy your `Shopify Webhook URL`

::callout{icon=i-mdi-navigation}
Navigate to **Store Admin > Settings > Notifications** on the Shopify website<br/>
:icon{name=i-mdi-chevron-right class="w-4 mr-1"} `https://admin.shopify.com/store/YOUR_STORE_NAME/settings/notifications`
::

1. Scroll to the bottom of the page and click `Create Webhook`
2. Set `Event` to `Order creation` or `Order payment`
    - You can create multiple webhooks if you would like to receive both events
3. Leave `Format` as `JSON`
4. Paste your `Shopify Webhook URL` from Streamer.bot into the `URL` field
5. Set the `Webhook API Version` to `Latest`
6. Click `Save`
7. You should now see a verification token highlighted in yellow - **copy this token**.

::callout{icon=i-mdi-navigation to="https://streamer.bot/user/settings#shopify" target=_blank rel=noopener}
Return to **Streamer.bot User Settings > Webhook Integrations > Shopify** on the Streamer.bot website
::

1. Paste the `Verification Token` into the `Shopify Verification Token` input

## Usage
::callout{icon=i-mdi-bookmark color=green to=/api/triggers/integrations/shopify/order-created}
Explore the [Shopify Triggers](/api/triggers/integrations/shopify/order-created) API references
::