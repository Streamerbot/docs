# Streamer.bot Documentation

![Streamer.bot Docs](https://img.shields.io/badge/docs-streamerbot?label=Streamer.bot&color=%239c59f1&link=https%3A%2F%2Fdocs.streamer.bot)
![Speaker.bot Docs](https://img.shields.io/badge/docs-speakerbot?label=Speaker.bot&color=%239c59f1&link=https%3A%2F%2Fspeaker.bot)
![Discord](https://img.shields.io/discord/834650675224248362?logo=discord&label=Discord&color=rgb(82%2C%2094%2C%20235))
![GitHub contributors](https://img.shields.io/github/contributors/Streamerbot/docs?logo=github&label=Contributors)
![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/Streamerbot/docs/deploy-streamerbot.yml)

Official home of all documentation content for [Streamer.bot](https://streamer.bot) and [Speaker.bot](https://speaker.bot)

## Contributing
Contributions are welcome and encouraged!

Feel free to open an issue to discuss missing information, or just fork and PR 💜

Guidelines: TBA

## Frontmatter
Some docs will be automatically built out from YAML frontmatter

### All
All pages should have a `title` and `description`.

Optionally, if the release version of a feature is known, the `version` key should contain the Streamer.bot version.

```yml
title: Page Title
description: Some description of this page
version: 0.2.3
```

### Sub-Actions & Triggers
The `variables` key will automatically build out the Variables section for these pages

```yml
twitchService: Chat Client
commonVariables:
  - TwitchUser
variables:
  - name: viewers
    type: number
    description: The amount of viewers this raid received
    value: 183
```

### C# Methods
Supplemental information can be added to C# methods:

```yml
parameters:
  - name: data
    description: |
      Data to be sent to connected clients

      JSON must be stringified.
    value: '"Hello, world!"'
```