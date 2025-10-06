---
title: Visual Studio Code
description: A guide to setting up Visual Studio Code for writing C# code for Streamer.bot with linting and autocomplete.
icon: mdi:microsoft-visual-studio-code
---

This tutorial provides a general step-by-step guide on setting up Visual Studio Code (VS Code) for writing C# code for Streamer.bot.

By following these instructions, you'll be able to write code with linting, which will help you catch errors early and ensure your code compiles before copying into Streamer.bot

## Prerequisites

::steps{level=3}
  ### Download & Install Visual Studio Code
  - [Download Visual Studio Code](https://code.visualstudio.com/download)
  - Follow the installation instructions for your operating system

  ### Configure Extensions
  - Launch Visual Studio Code if you haven't already
  - Open the Extensions menu
    - Keyboard Shortcut: `Ctrl+Shift+X`
    - Menu Bar: `View > Extensions`
  3. Install `IntelliCode for C# Dev Kit`
    - This dev kit will install all necessary extensions for C# development, including `C#`, `C# Dev Kit`, and `.NET Install Tool`

      ![image](https://gist.github.com/assets/8848167/80a7e6b0-86dd-4db0-87e2-801473a08d49)

  ### Sign in to Visual Studio Account
  1. Open Command Palette with
    - Keyboard Shortcut: `Ctrl+Shift+P`
    - Menu Bar: `View > Command Palette`
  2. Type `.NET: Sign into Visual Studio account` and select it

      ![image](https://gist.github.com/assets/8848167/b1ac3dde-177d-4576-babc-bd8635476dd4)

  3. Select `Allow` and it will open your web browser for you to log in with your Microsoft Account

      ![image](https://gist.github.com/assets/8848167/2fbc020b-abe2-4b35-a94c-0313f5081a81)

  4. Proceed to log in with Microsoft Account
::

## Create new .NET Project

1. Command Palette
   - Keyboard Shortcut: `Ctrl+Shift+P`
   - Menu Bar: `View > Command Palette`
2. Type `.NET: New Project` and select it

![image](https://gist.github.com/assets/8848167/56fd0378-3ba7-4dfd-a20d-9afeed9c0d68)

3. Select `Console App`

![image](https://gist.github.com/assets/8848167/8581a4ae-8a4b-41a4-ab9c-589805c51834)

4. Select a folder to save the new project folder into

5. Write a name for the project and hit enter

![image](https://gist.github.com/assets/8848167/4790ce9d-6758-4c1b-ade9-6a8b68aefe15)

6. Press enter or select `Create Project`

![image](https://gist.github.com/assets/8848167/6bc86d91-da60-4fcd-acbe-6885dd75616d)

7. Open the new project folder.
   - Keyboard Shortcut: `Ctrl+K, Ctrl+O`
   - Menu Bar: `File > Open Folder`

This is what you should see when you open the Explorer
![image](https://gist.github.com/user-attachments/assets/82d93eed-a5ac-4a39-8130-982aeb759181)

## Configure new project

1. Open the Explorer
   - Keyboard Shortcut: `Ctrl+Shift+E`
   - Menu Bar: `View > Explorer`
2. Navigate inside the open the `.csproj` file
3. Replace with this template in the code block below
4. Edit the Streamer.bot related dll filepaths to point to your Streamer.bot directory
5. Save and close the `.csproj` file

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>net472</TargetFramework>
    <ImplicitUsings>enable</ImplicitUsings>
    <LangVersion>latest</LangVersion>
    <NoWarn>CS0114</NoWarn> <!-- Ignore CS0114 errors -->
  </PropertyGroup>

  <ItemGroup>
    <!-- Include all DLLs in a specific directory in the build output -->
    <Reference Include="C:\Windows\Microsoft.NET\Framework64\v4.0.30319\System.dll" />
    <Reference Include="C:\Windows\Microsoft.NET\Framework64\v4.0.30319\System.Core.dll" />
    <Reference Include="C:\Windows\Microsoft.NET\Framework64\v4.0.30319\System.Net.dll" />
    <Reference Include="C:\Windows\Microsoft.NET\Framework64\v4.0.30319\System.Net.Http.dll" />
    <Reference Include="C:\Windows\Microsoft.NET\Framework64\v4.0.30319\netstandard.dll" />
    <Reference Include="C:\Windows\Microsoft.NET\Framework64\v4.0.30319\System.Windows.Forms.dll" />
    <Reference Include="C:\Windows\Microsoft.NET\Framework64\v4.0.30319\System.Drawing.dll" />
    <Reference Include="C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Microsoft.VisualBasic.dll" />
    <!-- List of dlls included with Streamer.bot -->
    <Reference Include="D:\overlays\streamerbot\Streamer.bot.Plugin.Interface.dll" />
    <Reference Include="D:\overlays\streamerbot\Streamer.bot.Common.dll" />
    <Reference Include="D:\overlays\streamerbot\Streamer.bot.Auth.dll" />
    <Reference Include="D:\overlays\streamerbot\Streamer.bot.EmoteHandlers.dll" />
    <Reference Include="D:\overlays\streamerbot\NAudio.dll" />
    <Reference Include="D:\overlays\streamerbot\NAudio.Core.dll" />
    <Reference Include="D:\overlays\streamerbot\Newtonsoft.Json.dll" />
    <Reference Include="D:\overlays\streamerbot\Twitch.Common.dll" />
    <Reference Include="D:\overlays\streamerbot\websocket-sharp.dll" />
    <!-- Example of a dll in the Streamer.bot dlls folder -->
    <!-- <Reference Include="D:\overlays\streamerbot\dlls\SharpOSC.dll" /> -->
  </ItemGroup>

</Project>
```

### .csproj Notes

- This file configures the project as a .NET Framework 4.7.2 project
- I've added some basic assembly references that are used frequently
- To point to your own Streamer.bot dlls, replace the directory with your own Streamer.bot directory and Streamer.bot `dlls` directory

## Template for the .cs file

1. Open the Explorer
   - Keyboard Shortcut: `Ctrl+Shift+E`
   - Menu Bar: `View > Explorer`
2. Navigate inside the open the `Program.cs` file
3. Replace your cs file with this template:

```cs
using Streamer.bot.Plugin.Interface;
using Streamer.bot.Plugin.Interface.Enums;
using Streamer.bot.Plugin.Interface.Model;
using Streamer.bot.Common.Events;
using System;

public class CPHInline : CPHInlineBase
{
    public bool Execute()
    {
        return true;
    }
}
```

### .cs Notes

- This is similar to the default code found in the `Execute C# Code` subaction
- The first four lines are required in VS Code, but are used by default and not needed in Streamer.bot
- Adding `: CPHInlineBase` after `public class CPHInline` seems to be the magic that gets VS Code to recognize the CPH methods (don't ask me why, I'm just a hobbyist programmer)

### You can now write code with assistance from IntelliCode

- You can type `CPH.` and it will automatically give you the available CPH methods
  - This uses the `Streamer.bot.Plugin.Interface.dll` of your Streamer.bot folder
  - The advantage of this is that you will have a current list of methods, classes, and enums available

![image](https://gist.github.com/assets/8848167/28c9fb4f-c368-487e-92f1-ff3e5eae95a1)

- Open `Problems`
  - Keyboard Shortcut: `Ctrl+Shift+M`
  - Menu bar: `View > Problems`
- The `Problems` view will show you if there will be any compile errors
  - Look for any red error icons

![image](https://gist.github.com/assets/8848167/53c1c7ae-824b-4210-a519-ba4cd3be1b00)

    - These errors will be compiler errors

  - You may notice some yellow warning icons

![image](https://gist.github.com/user-attachments/assets/17b86d3a-ab7d-4c32-84b5-21fa905f9f89)

    - These are only warnings and the code will still compile.

## Copying code to Streamer.bot

- Feel free to exclude the first four using statements from your code as they are automatically included in Streamer.bot's `Execute C# Code` subaction
- After copying and pasting your code into the `Execute C# Code` subaction dialog, remember to remove:

```text
: CPHInlineBase
```

from

```cs
public class CPHInline : CPHInlineBase
```

- Make sure the code compiles successfully by clicking `Compile`
- Click `Save and Compile`