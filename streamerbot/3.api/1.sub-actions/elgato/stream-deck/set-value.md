---
title: Set Value
description: Modify the value of a Status Indicator key or dial
parameters:
  - name: ElgatoStreamDeckButtonId
  - name: Value
    type: Number | Text
    description: |
      The new value for your selected [Status Indicator](https://streamdeck.streamer.bot/guide/keys#status-indicator)

      Supports text or numeric values, depending on your indicator configuration

      #### Special Values
      - **Reset Sparkline:** You can reset a `Sparkline` chart by sending an empty value
      - **Increment:** You can increment a numeric value by passing `+=[value]`, e.g. `+=1`
      - **Decrement:** You can decrement a numeric value by passing `-=[value]`, e.g. `-=1`
      - **Multiply:** You can multiply a numeric value by passing `*=[value]`, e.g. `*=1`
      - **Divide:** You can divide a numeric value by passing `/=[value]`, e.g. `/=1`
csharpMethods:
  - StreamDeckSetValue
---

::callout{icon=i-mdi-bookmark to=https://streamdeck.streamer.bot target=_blank}
Explore the full [Stream Deck Plugin Documentation](https://streamdeck.streamer.bot)
::
