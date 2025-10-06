---
name: CommandGetUserCounterById
title: CommandGetUserCounterById
description: Returns the total number of times a user has executed the specified command, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Define specified command via command id
            string commandId = "4fcc2d13-9bcf-4c18-9d91-821a15f4b6e5";
            //Get current user id
            CPH.TryGetArg("userId",out string userId);
            //Get current platform of user
            CPH.TryGetArg("userType",out string userType);
            Enum.TryParse(userType, out Platform platform);
            
            //Get CommandCounter
            CommandCounter commandCounterInfo = CPH.CommandGetUserCounterById(userId, platform, commandId);
            //Get command user count
            int numberOfUses = commandCounterInfo.Count;
            
            return true;
        }
    }
---
