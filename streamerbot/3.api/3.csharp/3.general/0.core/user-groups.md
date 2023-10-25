---
title: User Groups
description: C# methods for Streamer.bot user groups
---

## User in group
```csharp
bool UserIdInGroup(string userId, string groupName);
bool UserInGroup(int userId, string groupName);
bool UserInGroup(string userName, string groupName);
```

## Add user to group
```csharp
bool AddUserIdToGroup(string userId, string groupName);
bool AddUserToGroup(int userId, string groupName);
bool AddUserToGroup(string userName, string groupName);
```

## Remove user from group
```csharp
bool RemoveUserIdFromGroup(string userId, string groupName);
bool RemoveUserFromGroup(int userId, string groupName);
bool RemoveUserFromGroup(string userName, string groupName);
```