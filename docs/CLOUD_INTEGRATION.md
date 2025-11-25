# Cloud Integration

This doc explains how **GCP services** are wired to the MindsEye stack.

## BigQuery

- Long-horizon analytics
- Pattern scans over large event tables
- Materialized views for dashboards

## Cloud SQL

- Transactional workloads
- Smaller, low-latency tables (agents, configs, state)

## Firestore

- Realtime state for UI + agents
- Light-weight document storage

## GCS

- Raw event dumps
- Snapshots for reproducibility
- Training data for AI models

All of them are addressed via **MindsEye SQL**:

- `ROUTE bigquery`
- `ROUTE cloudsql`
- `ROUTE firestore`
- `ROUTE gcs`
