```cs
public class QuoteData
{
    public DateTime Timestamp { get; set; }

    public int Id { get; set; }

    public string UserId { get; set; }
    public string User { get; set; }
    public string Platform { get; set; }

    // GameId was removed in 1.0.0+ to make GameName
    // more flexible

    public string GameName { get; set; }

    public string Quote { get; set; }
}
```