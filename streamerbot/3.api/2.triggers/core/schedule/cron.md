---
title: Cron
description: Schedule a trigger using a Cron expression
version: 1.1.0

parameters:
  - name: Cron Expression
    type: string
    required: true
    description: |
      Enter a valid Cron expression to define the schedule.

variables:
  - name: expression
    type: string
    description: The Cron expression that defined the schedule for this trigger
    value: '0 0 * * *'

  - name: triggeredAt
    type: DateTime
    description: The timestamp when the Cron schedule was last triggered
    value: '8/22/2026 5:15:00 PM'
---
