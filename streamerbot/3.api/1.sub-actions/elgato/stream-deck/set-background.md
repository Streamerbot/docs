---
title: Set Background
description: Modify the background image of a Stream Deck key or dial
parameters:
  - name: ElgatoStreamDeckButtonId
  - name: Image
    type: Text
    description: |
      Image path or data used to update the background image of a Stream Deck button

      Supports any of the formats shown below:
      ::code-group
        ```bash [Local Path]
        C:\Users\John\Pictures\image.png
        ```
        ```bash [URL]
        https://api.iconify.design/mdi:alert.svg?color=%236312b5
        ```
        ```bash [Data URI]
        data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxZW0iIGhlaWdodD0iMWVtIiB2aWV3Qm94PSIwIDAgMjQgMjQiPjxwYXRoIGQ9Ik0xMyAxNGgtMlY5aDJtMCA5aC0ydi0yaDJNMSAyMWgyMkwxMiAyTDEgMjF6IiBmaWxsPSIjNjMxMmI1Ii8+PC9zdmc+
        ```
        ```html [SVG]
        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path d="M13 14h-2V9h2m0 9h-2v-2h2M1 21h22L12 2L1 21z" fill="#6312b5"/></svg>
        ```
      ::
  - name: Color
    type: Text
    description: |
      Set the background color of the given button.
      - When used in addition to the image field, the image will be placed on top of the selected color.
  - name: ElgatoStreamDeckButtonState
csharpMethods:
  - StreamDeckSetBackgroundColor
  - StreamDeckSetBackgroundUrl
  - StreamDeckSetBackgroundLocal
---

::read-more{to=https://streamdeck.streamer.bot}
Explore the full [Stream Deck Plugin Documentation](https://streamdeck.streamer.bot)
::
