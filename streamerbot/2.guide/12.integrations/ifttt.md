---
title: IFTTT
description: Bidirectional integration with IFTTT and Streamer.bot
navigation.icon: null
icon: arcticons:ifttt
version: 0.1.8
logo: https://streamer.bot/img/integrations/ifttt.png
---

Execute an action in Streamer.bot from any [IFTTT](https://ifttt.com) applet and/or send outgoing triggers from Streamer.bot to IFTTT.

::callout{color=amber icon=i-mdi-alert}
This integration requires the [Streamer.bot Website Integration](/guide/integrations/streamerbot)
::

## Configuration

1. Create a new applet in your IFTTT app
2. For `If This,` select the `Streamer.bot` service
3. Select the `IFTTT Notification Sub-Action` as your trigger
4. If you have not already, you will be asked to authenticate with your Streamer.bot account
5. Enter a matching event name in both your IFTTT applet and your Streamer.bot sub-action to trigger on specific events

## Usage

### Sub-Actions

Send outgoing triggers from Streamer.bot to IFTTT

::callout{icon=i-mdi-bookmark color=green to=/api/sub-actions/integrations/ifttt/notification}
Explore the [IFTTT Sub-Actions](/api/sub-actions/integrations/ifttt/notification) API references
::

---

### IFTTT Actions

::callout{icon=i-mdi-bookmark color=green to=https://ifttt.com/streamerbot target=_blank rel=noopener}
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