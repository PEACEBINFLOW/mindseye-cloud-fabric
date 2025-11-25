# minds eye cloud fabric

> Cloud wiring + automation blueprint for the entire MindsEye stack.

This repo answers one question:

> **“How does everything connect in the cloud?”**

It documents:

- How **MindsEye SQL** (`mindseye-sql-core`) runs across **BigQuery / Cloud SQL / Firestore / GCS**
- How events flow from:
  - Chrome extension
  - Android runtime
  - Binary engine
  - Moving Library
- How automations & agents use SQL as the **time-native epicenter**

## Overview

```txt
Chrome / Android / Agents
          ↓
   mindseye-data-splitter
          ↓
     mindseye-sql-core
          ↓
 BigQuery / Cloud SQL / Firestore / GCS
          ↓
 Ledger / Analytics / Devlog / Dashboard / Automations
