---
title: Users
description: Fetch Twitch user information from your code actions
---

## Methods

::callout{icon=i-mdi-alert color=amber}
The following Method requires the `0.2.3-alpha`.
::
### `TwitchGetBot`
:csharp-method{name=TwitchGetBot}

### `TwitchGetBroadcaster`
:csharp-method{name=TwitchGetBroadcaster}

### `TwitchGetExtendedUserInfoById`
:csharp-method{name=TwitchGetExtendedUserInfoById}

### `TwitchGetExtendedUserInfoByLogin`
:csharp-method{name=TwitchGetExtendedUserInfoByLogin}

### `TwitchIsUserSubscribed`
:csharp-method{name=TwitchIsUserSubscribed}

### `TwitchGetBitsDonatedByUserId`
:csharp-method{name=TwitchGetBitsDonatedByUserId}

### `TwitchGetUserInfoById`
:csharp-method{name=TwitchGetUserInfoById}

### `TwitchGetUserInfoByLogin`
:csharp-method{name=TwitchGetUserInfoByLogin}

## Classes
### The `TwitchUserInfo` Class
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

### The `TwitchUserInfoEx` Class
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
    public DateTime LastActive { get; set; }
    public DateTime PreviousActive { get; set; }
    public bool IsSubscribed { get; set; }
    public string SubscriptionTier { get; set; }

    public bool IsModerator { get; set; }
    public bool IsVip { get; set; }

    public DateTime CreatedAt { get; set; }
    public double AccountAge { get; set; }

    public string Game { get; set; }
    public string GameId { get; set; }

    public string ChannelTitle { get; set; }

    public List<string> Tags { get; set; }
}
```

