```csharp
public class GuestStar
{
    public string SlotId { get; set; }
    public bool IsLive { get; set; }
    public string UserId { get; set; }
    public string UserName { get; set; }
    public string UserLogin { get; set; }
    public int Volume { get; set; }
    public DateTime AssignedAt { get; set; }
    public MediaSettings AudioSettings { get; set; }
    public MediaSettings VideoSettings { get; set; }
}
```