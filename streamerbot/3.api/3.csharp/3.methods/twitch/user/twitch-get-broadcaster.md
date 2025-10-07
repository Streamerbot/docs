---
name: TwitchGetBroadcaster
title: TwitchGetBroadcaster
description: Get Twitch user information of connected broadcaster
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get user info
            TwitchUserInfo  userInfo = CPH.TwitchGetBroadcaster();

            //Get user login
            string userLogin = userInfo.UserLogin;
            //Get display name
            string user = userInfo.UserName;
            //Get user id
            string userId = userInfo.UserId;

            return true;
        }
    }
---