---
description: Remove all non-persisted global variables
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            CPH.ClearNonPersistedGlobals();

            return true;
        }
    }
---