---
title: UserVariableValue<T>
---

```cs
public class UserVariableValue<T>
{
  public string UserId
  public string UserName;
  public string UserLogin;
  public string UserType; //"Twitch","YouTube", "Trovo"...

  public string VariableName;
  public T Value;

  public DateTime LastWrite;
}
```