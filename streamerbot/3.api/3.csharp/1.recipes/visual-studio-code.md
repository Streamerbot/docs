---
title: Visual Studio Code
description: A guide to setting up Visual Studio Code for writing C# code for Streamer.bot with linting and autocomplete.
icon: mdi:microsoft-visual-studio-code
---

This tutorial provides a general step-by-step guide on setting up Visual Studio Code (VS Code) for writing C# code for Streamer.bot.

By following these instructions, you'll be able to write code with linting, which will help you catch errors early and ensure your code compiles before copying into Streamer.bot

::steps{level=2}
## Prerequisites

  ### Download & Install Visual Studio Code
  - [Download Visual Studio Code](https://code.visualstudio.com/download)
  - Follow the installation instructions for your operating system

  ### Configure Extensions
  - Launch Visual Studio Code if you haven't already
  - Open the Extensions menu
    - Keyboard Shortcut: `Ctrl+Shift+X`
    - Menu Bar: `View > Extensions`
  - Install `C#`
    - This is the necessary extension for C# development and includes the `.NET Install Tool`

      ![C# Extension in the extensions panel of Visual Studio Code](assets/vscode-csharp-extension.png)

## Create a new Streamer.bot Project Folder

1. Select `File > Open Folder` in the menu

    ![The Open Folder option being selected in VS Code's File menu](assets/vscode-open-folder-menu.png)

2. Select an empty folder, or create a new project folder, and then select it to open

    ![VS Code's Open Folder dialogue](assets/vscode-open-folder-dialogue.png)

## Create a `.csproj` File

1. Open the Explorer
   - Keyboard Shortcut: `Ctrl+Shift+E`
   - Menu Bar: `View > Explorer`
2. Create a New File

    ![New File option being selected in VS Code's Explorer Pane context menu](assets/vscode-new-file.png) 

3. Name the file, ending with `.csproj`

    ![A new file being named StreamerBot.csproj](assets/vscode-naming-new-csproj.png)

4. Paste the `Streamer.bot Project File Template` from the code block below
5. Replace the value of the `<StreamerBotPath>` xml tag to point to your Streamer.bot directory

::warning
Do not use quotes around your Streamer.bot directory path, even if it contains spaces.
::

6. Save and close the `.csproj` file

```xml [Streamer.bot Project File Template]
<Project Sdk="Microsoft.NET.Sdk">
   <PropertyGroup>
      <OutputType>Exe</OutputType>
      <TargetFramework>net481</TargetFramework>
      <LangVersion>13.0</LangVersion>
      <Nullable>enable</Nullable>
      <UseWPF>true</UseWPF>
      <DefineConstants>EXTERNAL_EDITOR</DefineConstants>
      <NoWarn>CS0114</NoWarn>

      <!-- Set the following directory with your Streamer.bot install location -->
      <StreamerBotPath>C:/path/to/streamer.bot-directory</StreamerBotPath>
   </PropertyGroup>
   <ItemGroup>
      <!-- Automatically include in every CS file -->
      <Using Include="Streamer.bot.Plugin.Interface" />
      <Using Include="Streamer.bot.Plugin.Interface.Model" />
      <Using Include="Streamer.bot.Plugin.Interface.Enums" />
      <Using Include="Streamer.bot.Common.Events" /> 

      <!-- Use forward slashes for cross-platform compatibility -->
      <Reference Include="$(StreamerBotPath)/Streamer.bot.Plugin.Interface.dll" />
      <Reference Include="$(StreamerBotPath)/Streamer.bot.Common.dll" />
      <Reference Include="$(StreamerBotPath)/Twitch.Common.dll" />

      <Reference Include="$(StreamerBotPath)/NAudio*.dll" />
      <Reference Include="$(StreamerBotPath)/Wpf*.dll" />
      <Reference Include="$(StreamerBotPath)/Newtonsoft.Json.dll" />

      <!-- Uncomment the following line to reference all dlls in the streamerbot directory -->
      <!-- <Reference Include="$(StreamerBotPath)/**/*.dll" /> -->
   </ItemGroup>
</Project>
```

### `.csproj` Notes

- This file includes the Streamer.bot using statements in every `.cs` file automatically
- This file configures the project as a .NET Framework 4.8.1 project
- To point to your own Streamer.bot dlls, replace the contents of `<StreamerBotPath>` with the path to your own Streamer.bot directory (containing `Streamer.bot.exe` and `.dll` files)

## Template for the `.cs` file

1. Open the Explorer
   - Keyboard Shortcut: `Ctrl+Shift+E`
   - Menu Bar: `View > Explorer`
2. Create a new file ending with the `.cs` extension

   ![A new file being named MyAction.cs](assets/vscode-naming-new-cs-file.png)

3. Paste the `C# Code Example` below into your `.cs` file, replacing `UniqueClassName` with your FileName:
4. You can also create a file template as a workplace snippet, to make inserting this into new files easier:
    - Open the Command Palette with `Ctrl+Shift+P` and select `Snippets: Configure Snippets`
      ![VS Code Command Palette with Snippets: Configure Snippets selected](assets/vscode-configure-snippets-command.png)
    - Select the option to create a new snippets file for the current workspace, and enter a filename like `sbSnippets`
      ![VS Code Configure Snippets Command with New Snippets file for workspace option selected](assets/vscode-snippets-new-workplace-file.png)
    - Replace the contents of your new `.code-snippets` file with the `File Template Snippet` below
    - After creating new .cs files, you can now fill them with the snippet by either typing `sbfile`, and selecting the `streamer.bot-file-template` from the dropdown, or by running `Snippets: Fill File with Snippet` from the Command Palette

::code-group
```cs [C# Code Example]
using System;

/*----- Class name should match FileName -----*/
#if EXTERNAL_EDITOR
public class UniqueClassName : CPHInlineBase
#else
public class CPHInline
#endif
/*--------------------------------------------*/
{
    public bool Execute()
    {
        // Add your code here
        return true;
    }
}
```
```json [File Template Snippet]
{
    "Execute C# Sub-Action Template" : {
		"scope": "csharp",
        "isFileTemplate": true,
        "prefix": "streamer.bot-file-template",
        "description": "New Execute C# Sub-Action for Streamer.bot",
        "body": [
            "using System;",
            "",
            "/*----- Class name should match FileName -----*/",
            "#if EXTERNAL_EDITOR",
            "public class ${TM_FILENAME_BASE} : CPHInlineBase",
            "#else",
            "public class CPHInline",
            "#endif",
            "/*--------------------------------------------*/",
            "{",
            "    public bool Execute()",
            "    {",
            "        ${0:// Add your code here}",
            "        return true;",
            "    }",
            "}"
        ]
    }
}
```
::

### `.cs` Notes

- This is similar to the default code found in the `Execute C# Code` subaction
- The first four lines are required in VS Code, but are used by default and not needed in Streamer.bot
- The `#if EXTERNAL_EDITOR` preprocessor directive is set to true by the `.csproj` we just created, but is not active in Streamer.bot's editor.
  - In VS Code, each class name in a project must be unique, so changing `UniqueClassName` to the FileName avoids conflicts, while explicitly inheriting from `CPHInlineBase`, the class which provides the `CPH` instance all of our Streamer.bot methods belong to.
  - In Streamer.bot, the class must be called `CPHInline`, which automatically inherits from `CPHInlineBase`.

::

### You can now write code with assistance from IntelliSense

- You can now type `CPH.` and it will automatically give you the available `CPH` methods
  - This uses the `Streamer.bot.Plugin.Interface.dll` in your Streamer.bot folder
  - The advantage of this is that you will have an up-to-date list of methods, classes, and enums available

![Dropdown of autocomplete options following CPH. in VS Code](assets/vscode-example-autocomplete.png)

- Open `Problems`
  - Keyboard Shortcut: `Ctrl+Shift+M`
  - Menu bar: `View > Problems`
- The `Problems` view will show you if there will be any compile errors
  - Look for any red error icons

  ![Example of missing semicolon error which will not compile](assets/vscode-example-error.png)

::caution
These errors will be compiler errors
::
  - You may notice some yellow warning icons

  ![Example of compiler warning for an unused variable which will not block compilation](assets/vscode-example-warning.png)

::warning
These are only warnings and the code will still compile.
::

## Copying Code to Streamer.bot
- Create an `Execute C# Code` Sub-Action
- You can copy the entirety of your `.cs` file into Streamer.bot's editor.
    - The preprocessor directives will keep the sections which are only needed for VS Code from being active inside Streamer.bot.
- Make sure the code compiles successfully by clicking `Compile`
- Click `Save and Compile`

::tip{color=primary}
If you see any errors ending with `(are you missing an assembly reference?)`, click `Find Refs`
::

::success
Your code has now been added inside an `Execute C# Code` Sub-Action and is ready to run in your Action!
::