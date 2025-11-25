# Automations Map

This map shows **which automations run where**, and how they hit MindsEye SQL.

- `mindseye-automations`:
  - calls `mindseye-sql-core` to:
    - compute triggers
    - fetch segments (users, sessions)
    - store automation logs

- `mindseye-google-ledger`:
  - reads from `ROUTE bigquery` tables
  - writes to GCS for long-term snapshots

- `mindseye-google-analytics`:
  - pulls views for dashboards
  - uses `TIMELINE` and `pattern()` heavily

- `mindseye-google-devlog`:
  - stores meta-events about system runs
  - all time-labeled and queryable via SQL
