---
name: NextDouble
title: NextDouble
description: Returns a double type between 0 and 1. Often used for random percentages
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            double percent = CPH.NextDouble();
            CPH.SetArgument("decimalPercent",percent);
            
            return true;
        }
    }
---