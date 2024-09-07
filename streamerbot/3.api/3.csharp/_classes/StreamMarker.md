```cs
public class StreamMarker
{
    public string Id { get; set; }
    public DateTime CreatedAt { get; set; }
    public string Description { get; set; }
    //Position in seconds of stream marker
    public int Position { get; set; }
}
```