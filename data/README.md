# Data directories

| Directory | Purpose | Git policy |
|---|---|---|
| `external/` | Immutable third-party datasets and metadata | Ignored |
| `raw/` | Immutable synthetic or source-system-style exports | Ignored |
| `interim/` | Reproducible working tables | Ignored |
| `processed/` | Analysis-ready marts and model outputs | Ignored |
| `sample/` | Small, non-sensitive fixtures for examples and tests | May be committed |

Raw and external files must never be edited in place. Future acquisition scripts
will record source URLs, retrieval dates, versions, checksums, licenses, and any
simulation seed. A formal data dictionary will live in `docs/`.
