```cs
public class TwitchUserInfoEx
{
  public string UserName { get; set; }
  public string UserLogin { get; set; }
  public string UserId { get; set; }
  public string Description { get; set; }
  public string ProfileImageUrl { get; set; }
  public string UserType { get; set; }

  public bool IsPartner => string.Equals(UserType, "partner", StringComparison.OrdinalIgnoreCase);
  public bool IsAffiliate => string.Equals(UserType, "affiliate", StringComparison.OrdinalIgnoreCase);

  public bool IsFollowing { get; set; }
  public bool IsSubscribed { get; set; }
  public string SubscriptionTier { get; set; }

  public bool IsModerator { get; set; }
  public bool IsVip { get; set; }

  public DateTime LastActive { get; set; }
  public DateTime PreviousActive { get; set; }
  public DateTime CreatedAt { get; set; }
  public double AccountAge { get; set; }

  public string Game { get; set; }
  public string GameId { get; set; }

  public string ChannelTitle { get; set; }

  public List<string> Tags { get; set; }
}
```
