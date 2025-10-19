---
name: Persisted
type: Toggle
default: true
---

Toggle between `Persisted` and `Non-Persisted` variables

- `Persisted` - These variables persist across Streamer.bot restarts
- `Non-Persisted` - These variables should be considered **temporary** and will be wiped at shutdown

::warning
Ensure you select the correct datastore (persisted or non-persisted) for the variable you are trying to get or set
::