---
name: Persisted
type: Toggle
default: Persisted
options:
  - value: Persisted
    description: These variables persist across Streamer.bot restarts
  - value: Non-Persisted
    description: These variables should be considered **temporary** and will be wiped at shutdown
---

Toggle between `Persisted` and `Non-Persisted` variables

::warning
Ensure you select the correct datastore (persisted or non-persisted) for the variable you are trying to get or set
::