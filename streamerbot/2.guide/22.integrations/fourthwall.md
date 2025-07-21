---
title: Fourthwall
description: Integrate Streamer.bot with your Fourthwall account
navigation.icon: null
version: 0.2.3
logo: /img/icons/fourthwall.png
---

Receive [Fourthwall](https://fourthwall.com) event triggers in Streamer.bot via webhooks

::warning
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

1. Get your Fourthwall Webhook URL

    ::navigate{to="https://streamer.bot/user/settings#fourthwall" target=_blank rel=noopener}
    Navigate to **User Settings > Webhook Integrations > Fourthwall** on the Streamer.bot website
    ::

    1. Set `Fourthwall Connection` to `Enabled`
    2. Copy your `Fourthwall Webhook URL`

2. Configure Fourthwall Webhooks and obtain secret token

    ::navigate
    Navigate to **Fourthwall Dashboard > Settings > For Developers** on the Fourthwall website<br/>
    :icon{name=i-mdi-chevron-right class="w-4 mr-1"} `https://<YOUR_SHOP_NAME>.fourthwall.com/admin/dashboard/settings/for-developers`
    ::

    1. Click `Create webhook`
    2. Paste your `Fourthwall Webhook URL` from Streamer.bot into the `URL` field
    3. Select the events you want to receive
    4. Click `Save`
    5. You should see a secret token at the bottom of the page - **copy this token**

3. Add your Fourthwall Secret

    ::navigate{to="https://streamer.bot/user/settings#fourthwall" target=_blank rel=noopener}
    Return to **User Settings > Webhook Integrations > Fourthwall** on the Streamer.bot website
    ::

    1. Paste the secret token into the `Fourthwall Webhook Secret` input

4. Done!

    ::success
    Fourthwall events should now be available as triggers in Streamer.bot!
    ::

## Usage
:api-reference-cards{path=integrations/fourthwall}