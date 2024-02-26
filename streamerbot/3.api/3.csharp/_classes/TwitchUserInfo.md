```cs
public class TwitchUserInfo
{
  public string UserName { get; set; }
  public string UserLogin { get; set; }
  public string UserId { get; set; }

  public DateTime LastActive { get; set; }
  public DateTime PreviousActive { get; set; }

  public bool IsSubscribed { get; set; }
  public string SubscriptionTier { get; set; }

  public bool IsModerator { get; set; }
  public bool IsVip { get; set; }
}
```