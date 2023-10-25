# Execute C# Method
Directly call into C# methods defined in your [Execute Code](csharp-execute-code) sub-actions

Using this sub-action, you can call into an existing execute code, and call another method, or it's main entry point.

If you have the Execute C# Code setup for `Keep Alive` and `Precompile on Startup` you can use `private` variables within the class to preserve data between calls.

The methods must be in the form of a return type of `bool` with no parameters:

```csharp
public bool MethodName()
{
    // your code here
    return true;
}
```

> The capabilities of this sub-action may be extended later.