# High-Level Architecture

```txt
+-------------------------------+
|         Client Layer          |
|-------------------------------|
| Chrome Agent Shell            |
| Android LAW-T Runtime         |
| IoT / Edge Devices            |
+-------------------------------+
                 |
                 v
+-------------------------------+
|       Ingest / Splitter       |
| (mindseye-data-splitter,     |
|  minds-eye-law-n-network)    |
+-------------------------------+
                 |
                 v
+-------------------------------+
|       MindsEye SQL Core       |
|      (mindseye-sql-core)      |
+-------------------------------+
        |        |        |
        v        v        v
   BigQuery   Cloud SQL  Firestore
        \        |        /
         \       |       /
          \      |      /
             +--------+
             |  GCS   |
             +--------+

Downstream:

- mindseye-google-ledger
- mindseye-google-analytics
- mindseye-google-devlog
- dashboards, agents, automations
