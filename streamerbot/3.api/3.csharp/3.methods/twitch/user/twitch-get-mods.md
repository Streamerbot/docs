---
name: TwitchGetMods
title: TwitchGetMods
description: Get a list of all users currently assigned as moderators in the broadcaster's Twitch channel.
version: 1.0.7
example: |
  using System;
  using System.Collections.Generic;

  public class CPHInline
  {
      public bool Execute()
      {
          //get the list of Mods for the channel
          List<TwitchUserInfo> mods = CPH.TwitchGetMods();

          //iterate through the list and log the username and user id of each Moderator
          foreach (TwitchUserInfo mod in mods)
          {
              CPH.LogInfo($"Moderator: {mod.UserName} ({mod.UserId})");
          }

          return true;
      }
  }
---
