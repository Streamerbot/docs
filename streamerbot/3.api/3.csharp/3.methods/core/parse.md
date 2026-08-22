---
name: Parse
title: Parse
description: Parse a string and replace variables using the provided arguments.
version: 1.0.7
example: |
    using System;
    using System.Collections.Generic;

    public class CPHInline
    {
        public bool Execute()
        {
            //create a dictionary of arguments to be used for parsing
            var args = new Dictionary<string, object>
            {
                ["userName"] = "MustachedManiac",
                ["userId"] = 123456789,
                ["isModerator"] = true,
                ["points"] = 1500
            };

            //parse the string and replace the variables with the provided arguments
            string result = CPH.Parse(
                "User: %userName% | ID: %userId% | Moderator: %isModerator% | Points: %points%",
                args
            );

            //log the result to see the parsed string with replaced variables
            CPH.LogInfo(result);

            return true;
        }
    }
---