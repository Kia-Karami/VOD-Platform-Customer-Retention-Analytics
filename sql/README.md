# SQL layers

SQL transformations follow a one-way dependency flow:

1. `staging/` cleans source fields, standardizes types, and records exclusions.
2. `intermediate/` creates reusable behavioral features and event-level logic.
3. `marts/` builds customer, retention, catalog, and candidate-movie tables.
4. `analyses/` answers business questions and validates final outputs.

Queries should be deterministic, documented, and compatible with DuckDB. Metric
definitions belong in `docs/`; SQL comments should explain implementation choices.
