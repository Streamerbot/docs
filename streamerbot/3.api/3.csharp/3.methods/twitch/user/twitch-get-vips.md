---
name: TwitchGetVips
title: TwitchGetVips
description: Get a list of all users currently assigned as VIPs in the broadcaster's Twitch channel.
version: 1.0.7
example: |
  using System;
  using System.Collections.Generic;

  public class CPHInline
  {
      public bool Execute()
      {
          //get the list of VIPS for the channel
          List<TwitchUserInfo> vips = CPH.TwitchGetVips();

          //iterate through the list and log the username and user id of each VIP
          foreach (TwitchUserInfo vip in vips)
          {
              CPH.LogInfo($"VIP: {vip.UserName} ({vip.UserId})");
          }

          return true;
      }
  }
---
