---
title: Fourthwall
description: Integrate Streamer.bot with your Fourthwall account
navigation.icon: null
version: 0.2.3
badge: New
logo: /img/icons/fourthwall.png
---

Receive [Fourthwall](https://fourthwall.com) event triggers in Streamer.bot via webhooks

::callout{color=amber icon=i-mdi-alert}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

::callout{icon=i-mdi-navigation to="https://streamer.bot/user/settings#fourthwall" target=_blank rel=noopener}
Navigate to **Streamer.bot User Settings > Webhook Integrations > Fourthwall** on the Streamer.bot website
::

1. Set `Fourthwall Connection` to `Enabled`
2. Copy your `Fourthwall Webhook URL`

::callout{icon=i-mdi-navigation}
Navigate to **Fourthwall Dashboard > Settings > For Developers** on the Fourthwall website<br/>
:icon{name=i-mdi-chevron-right class="w-4 mr-1"} `https://<YOUR_SHOP_NAME>.fourthwall.com/admin/dashboard/settings/for-developers`
::

1. Click `Create webhook`
2. Paste your `Fourthwall Webhook URL` from Streamer.bot into the `URL` field
3. Select the events you want to receive
4. Click `Save`
5. You should see a secret token at the bottom of the page - **copy this token**

::callout{icon=i-mdi-navigation to="https://streamer.bot/user/settings#fourthwall" target=_blank rel=noopener}
Return to **Streamer.bot User Settings > Webhook Integrations > Fourthwall** on the Streamer.bot website
::

1. Paste the secret token into the `Fourthwall Webhook Secret` input

## Usage
:api-reference-cards{path=integrations/fourthwall}