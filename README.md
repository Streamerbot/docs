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

## MDC Components

The following are preconfigured `::callout` components:

```
::note
This is some useful information to callout
::

::tip
This is a cool tip!
::

::warning
Some important info goes here
::

:read-more{to="/path/to/some/other/page"}

::wip
This content is a work in progress
::
```


## Frontmatter
Some docs will be automatically built out from YAML frontmatter

### All
All pages should have a `title` and `description`.

Optionally, if the release version of a feature is known, the `version` key should contain the Streamer.bot version it was added in.

```yml
title: Page Title
description: Some description of this page
version: 0.2.3
```

### Sub-Actions & Triggers
Variables, Parameters (e.g. Sub-Action dialog options), and C# Method sections can automatically be built from front matter keys:

```yml [api/sub-actions/my-sub-action.md]
twitchService: Chat Client
parameters:
  - name: Game Title
    type: Text
    required: true
    description: |
      Enter the description for this parameter with full markdown support.

      ::tip
        It even supports mdc!
      ::
  - name: Some other parameter
    type: Select
    required: false
    description: This is the description for some other parameter
variables:
  - name: viewers
    type: number
    description: The amount of viewers this raid received
    value: 183
commonVariables:
  - TwitchUser
csharpMethods:
  - UnbanUser
  - BanUser
```

### C# Methods
Supplemental information can be added to C# methods by adding a markdown file into the api/csharp/_methods directory with the **exact same name** as the C# Method:


```md [_methods/SomeCsharpMethod.md]
---
description: The primary short description for SomeCsharpMethod
version: 0.2.3
parameters:
  - name: data
    description: |
      Data to be sent to connected clients

      JSON must be stringified.
    value: '"Hello, world!"'
---

Some extended description information
```

- `description` - Short description rendered **above** the resulting C# code block and included in SEO
- `version` - Optional value representing the version of Streamer.bot that added this feature
- `deprecated` - Optional value representing the version of Streamer.bot that deprecated this feature
- `parameters` - Optional of parameter documentation
    - `name` - The exact name of this parameter. **Must match the name from Streamer.bot**
    - `description` - Any additional documentation or info to include with this parameter. **Markdown supported**
    - `value` - An example C# value for this parameter. Will be used within the `CPH Example` code block and included in the `Copy` function
    - `import` - Optionally import the parameter fields above from a file in the  _parameters dir (see below)

### C# Parameters
Additionally, parameters information can be shared by referencing the name of any markdown or yaml file in the api/csharp/_parameters directory:

```md [_methods/SomeCsharpMethod.md]
---
parameters:
  - import: SomeSharedParameter
---
```

```md [_paramters/SomeSharedParamter]
---
name: my_parameter
description: |
  Some long description

  With extra info

  That would be annoying to include in every file that uses this parameter 😉
value: 0
---
```