```cs
public class TwitchReward
{
    public string Id { get; set; }
    public string Title { get; set; }

    public string Group { get; set; }

    public string Prompt { get; set; }
    public int Cost { get; set; }
    public bool InputRequired { get; set; }
    public string BackgroundColor { get; set; }

    public bool Paused { get; set; }
    public bool Enabled { get; set; }
    public bool IsOurs { get; set; }
}
```