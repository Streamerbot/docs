```cs
public class TwitchRewardCounter
{
    public string UserId { get; set; }
    public string UserLogin { get; set; }
    public string UserName { get; set; }

    public int Count { get; set; }

    public DateTime LastRedeemed { get; set; }
}
```