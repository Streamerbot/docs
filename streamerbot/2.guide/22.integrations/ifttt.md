---
title: IFTTT
description: Bidirectional integration with IFTTT and Streamer.bot
navigation.icon: null
icon: simple-icons:ifttt
version: 0.1.8
logo: https://streamer.bot/img/integrations/ifttt.png
---

Execute an action in Streamer.bot from any [IFTTT](https://ifttt.com) applet and/or send outgoing triggers from Streamer.bot to IFTTT.

::warning
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Send Notifications to IFTTT

Utilize Streamer.bot to trigger 3rd party services via IFTTT

1. If This...

    ::navigate
    In the IFTTT Application, select **Create** to create a new applet
    ::

    1. For `If This,` select the `Streamer.bot` service
    2. Select the `IFTTT Notification Sub-Action` as your trigger
        - This will allow IFTTT to **receive** events from Streamer.bot

2. Authenticate with Streamer.bot

    1. If you have not already, you will be asked to authenticate with your Streamer.bot account
    2. Select your authenticated Streamer.bot account
    3. Enter a unique event name to listen for specific notifications from Streamer.bot

3. Then That...

    Select any service you want to trigger!

4. Add a IFTTT Notification Sub-Action

    ::navigate
    In Streamer.bot, add an IFTTT Notification sub-action to a new or existing action
    ::

    1. Enter the same event name you entered in the IFTTT applet
    2. Enter any text you want to send to IFTTT for use in other applets!

5. Done!

    ::success
    Streamer.bot can now send events to IFTTT!
    ::

## Execute Actions with IFTTT

Utilize IFTTT to trigger Streamer.bot actions from 3rd party services

1. If This...

    ::navigate
    In the IFTTT Application, select **Create** to create a new applet
    ::

    1. For `If This,` select the your desired service
        - For example, we are going to pick the `Button widget` service
    2. Select your desired trigger from the selected service
        - We are going to use the `Button press` trigger

2. Then That...

    1. After `Then That`, click `Add`
    2. Search for and select the `Streamer.bot` service
    3. Select the `Execute Action` IFTTT action

2. Authenticate with Streamer.bot

    1. If you have not already, you will be asked to authenticate with your Streamer.bot account
    2. Select your authenticated Streamer.bot account

3. Configure your Streamer.bot action

    1. Under `Action`, select your Streamer.bot instance you want to trigger
    2. Select the Streamer.bot action you want to execute
    3. Enter any text to include as an argument when executing the action

4. Done!

    ::success
    IFTTT can now execute actions in your Streamer.bot instance!
    ::


## Usage
:api-reference-cards{path=integrations/ifttt}

---

## IFTTT Actions

::read-more{to=https://ifttt.com/streamerbot target=_blank rel=noopener}
Explore the [Streamer.bot Service](https://ifttt.com/streamerbot) on IFTTT
::

#### Execute Action
The `Execute Action` IFTTT action allows you to execute any action in your Streamer.bot instance along with a configurable text field.

The following arguments will be made available to your Streamer.bot actions:

Name | Description
----:|:------------
`iftttText` | The contents of the `Text` field from your IFTTT applet. This can include any ingredients from other IFTTT supported services in your applet.

#### Execute Action (JSON)
The `Execute Action (JSON)` IFTTT action allows you to execute any action in your Streamer.bot instance with a JSON payload that is automatically parsed into variables for usage in your Streamer.bot sub-actions.

This is extremely useful for connecting generic webhooks with Streamer.bot through the [IFTTT Webhooks Integration](https://ifttt.com/maker_webhooks).

All top level keys in the JSON payload passed to this action will be available as variables in Streamer.bot

For example, the following JSON payload...
```json
{ "test": "some value", "test2": "some other value" }
```
...will be transformed into the variables `test` and `test2`, which will be populated with their respective values.