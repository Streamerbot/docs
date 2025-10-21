---
title: Set Value
description: Modify the value of a Status Indicator key or dial
parameters:
  - name: Button ID
    import: elgato/stream-deck-button-id
  - name: Value
    type: Number | Text
    description: |
      The new value for your selected [Status Indicator](https://streamdeck.streamer.bot/guide/keys#status-indicator)

      Supports text or numeric values, depending on your indicator configuration

      <br>

      **Special Values**

      You can also use the following special formats to modify existing numeric values:

      | Operation | Format | Example |
      | --- | --- | --- |
      | Reset Sparkline | Empty value | ` ` |
      | Increment | `+=[value]` | `+=1` |
      | Decrement | `-=[value]` | `-=1` |
      | Multiply | `*=[value]` | `*=1` |
      | Divide | `/=[value]` | `/=1` |
csharpMethods:
  - StreamDeckSetValue
---

::read-more{to=https://streamdeck.streamer.bot}
Explore the full [Stream Deck Plugin Documentation](https://streamdeck.streamer.bot)
::
