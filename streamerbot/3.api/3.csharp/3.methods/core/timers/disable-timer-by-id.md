---
name: DisableTimerById
title: DisableTimerById
description: Disables selected timer, by ID
version: 0.2.4
example: |
    using System;
    public class CPHInline
    {
        public bool Execute()
        {
            //Guid are convertable directly to string since 0.2.5
            CPH.TryGetArg("timerId",out string timerId);
            //Otherwise use the commented out methods below to get the current timerId
            //CPH.TryGetArg<Guid>("timerId", out var timerIdVar);
            //string timerId = timerIdVar.ToString();
            
            CPH.DisableTimerById(timerId);
            
            return true;
        }
    }
---
