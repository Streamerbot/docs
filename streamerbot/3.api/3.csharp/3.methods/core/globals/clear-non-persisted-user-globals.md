---
name: ClearNonPersistedUserGlobals
title: ClearNonPersistedUserGlobals
description: Remove all non-persisted global user variables
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            CPH.ClearNonPersistedUserGlobals();

            return true;
        }
    }
---