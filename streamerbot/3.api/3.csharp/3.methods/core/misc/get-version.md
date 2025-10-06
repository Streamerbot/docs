---
name: GetVersion
title: GetVersion
description: Returns the SemVersion of the current Streamer.bot installation
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Get version string in SemVersion format (0.2.6)
            string sbVersion = CPH.GetVersion();
            //Write to log
            CPH.LogInfo(sbVersion);
            
            return true;
        }
    }
---
