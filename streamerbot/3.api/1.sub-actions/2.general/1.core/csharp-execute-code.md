# Execute C# Code
For the power users out there, I've included the ability for runtime compilation of your own code to act as an action!

Whenever you add a new Execute C# code action, you will be greeted with the following code snippet:

```csharp
using System;

public class CPHInline
{
    public bool Execute()
    {
        // your main code goes here
        return true;
    }
}
```

For every execute code sub-action, this is the minimum that must be present for it to function.

You can also have an `Init()` and a `Dispose()` method that will be called when your code is first compiled, and when it is destroyed, so if you need to do any initialization steps, or cleanup steps, you'll be able to, **THESE TWO METHODS ARE OPTIONAL**.

You will want to add the following for init:

```csharp
public void Init()
{
    // place your init code here
}
```

And the following for dispose:

```csharp
public void Dispose()
{
    // place your dispose code here
}
```

You will be able to make calls to internal Streamer.bot methods using a special `CPH` class.  You can see all the available methods at:

* [Available Methods](/Sub-Actions/Code/CSharp/Available-Methods)
{.links-list}

{.is-info}
> CPH Refers to the Development name for Streamer.bot - `ChannelPointsHandler`
{.is-info}


## Compiling Log
Shows some general information based on what buttons you've pressed, this will show any compiler errors, and general information when trying to find references

## References
List the references required for compiling your code, you can right click to add specific references

## Settings

### Name
Set a descriptive name for your Execute Code sub-action for a quick glance at what it does

### Description
Set a longer description of what your Execute Code sub-action does

### Keep Instance Active
By ticking this option, your code will be kept alive for the lifetime of the application, this will allow you to preserve data between calls to this sub-action

### Precompile on Application Start
By ticking this, your code will be automatically compiled when you start Channel Points Handler so it is ready to go, instead of the first time the sub-action is ran

## Available Buttons

### Format Document
This will auto-tab your document to make thing look a bit nicer

### Find Refs
Will attempt to auto find some common references based on your `using` directives, this capability is still evolving, and sometimes is not very smart.

### Compile
Test the compilation of your code, see if it compiles clean.  A small note on this, it will also remove any references that are unused, this is can also be a bit, stange at times, and may wind up removing a reference that is actually needed.  Much like the Find Refs, this is evolving as well.

### Save and Compile
This will save your changes, and pre-compile the code so its ready to go the first time the action is hit

### Ok
Save your changes

### Cancel
Discard your changes

## Video Tutorials
This video's are video's for learning C# with streamer.bot{.subtitle}

<section class="overview-grid my-5">
<div>

nutty VODs{.overline}

<span></span>

<div class=“iframe-container”><iframe src="https://www.youtube.com/embed/rS5ZuIZV_y0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; fullscreen" allow fullscreen style="border: none; max-width: 100%; width: 100%; aspect-ratio: 16/9;"></iframe></div>

</div>
  <div>

TerrierDarts{.overline}

<span></span>

<div class=“iframe-container”><iframe src="https://www.youtube.com/embed/videoseries?list=PLVmWn5RfnNsogzpk5loBoYXvWEZY-Qz6g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; fullscreen" allow fullscreen style="border: none; max-width: 100%; width: 100%; aspect-ratio: 16/9;"></iframe></div>
    </div>
</section>

---

- [<i class="mdi mdi-chevron-left"></i> **Code *Go Back***](/Sub-Actions/Code)
{.btn-grid .my-5}