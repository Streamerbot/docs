---
description: Returns all commands associated with Streamer.bot instance
version: 0.2.5
example: |
    using System;
    using System.Collections.Generic;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get list of actions
            List<CommandData> commandList = CPH.GetCommands();
            
            //Example to go through list and write each command to logfile
            foreach(CommandData command in commandList)
            {
                //Get id of current command
                //Due to it being Guid type need to convert to string.
                string id = command.Id.ToString();
                //Get name of current command
                string name = command.Name;
                //Write to log
                CPH.LogInfo($"CommandId:{id}, Command Name: {name}");
            }
            return true;
        }
    }
---