The CPH method uses the [SendKeys](<https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.sendkeys.send?view=windowsdesktop-7.0>) method. That means the `keyPress` string needs to be enclosed in curly brackets `{}`. To use key combinations (`SHIFT`, `CTRL` and `ALT`) you can use code modifiers listed in the link or the examples below.

Examples:

1. Pressing the `W` key
```cs
CPH.KeyboardPress("{W}");
```

2. Pressing the `DOWN ARROW` key
```cs
CPH.KeyboardPress("{DOWN}");
```

3. Pressing `SHIFT` and `W`
```cs
CPH.KeyboardPress("+{W}");
```

4. Pressing `CTRL` and `W`
```cs
CPH.KeyboardPress("^{W}");
```

5. Pressing `ALT` and `W`
```cs
CPH.KeyboardPress("%{W}");
```
