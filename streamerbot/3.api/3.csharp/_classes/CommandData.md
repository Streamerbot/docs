```cs
public class CommandData
{
public Guid Id { get; set; }
public string Name { get; set; }
public bool Enabled { get; set; }
public string Group { get; set; }
public int Mode { get; set; }

public List<string> Commands { get; set; }
public string RegexCommand { get; set; }

public bool CaseSensitive { get; set; }

public List<string> Sources { get; set; }
}
```
