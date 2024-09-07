---
description: Get Twitch extended user information of specified user id
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get user id of current user
            CPH.TryGetArg("userId",out string userId);

            //Get user info
            TwitchUserInfoEx userInfo = CPH.TwitchGetExtendedUserInfoById(userId);

            //Get user profile image url
            string imageUrl = userInfo.ProfileImageUrl;
            //Get current game of user
            string game = userInfo.Game;
            //Get DateTime when user was created on Twitch
            DateTime createdAt = userInfo.CreatedAt;

            return true;
        }
    }
---