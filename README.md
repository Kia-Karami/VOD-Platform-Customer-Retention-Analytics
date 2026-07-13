# VOD Platform Customer Retention Analytics

> Reducing catalog-exhaustion risk through power-user segmentation and
> data-driven content acquisition.

This repository is a reconstructed analytics portfolio case study inspired by a
simulated Rahnama College Data Analyst Bootcamp scenario. It does **not** contain
data from a real commercial VOD company, and offline estimates will not be
presented as causal business impact.

## Business challenge

A transactional video-on-demand platform can acquire no more than 1,000 new
movies. The project will identify the portfolio most likely to protect valuable
customers and future revenue while maintaining a relevant, diverse catalog.

The analysis will test—rather than assume—the proposed behavioral chain:

`high consumption -> faster catalog exhaustion -> declining activity -> churn risk`

## Project status

**Stage 0: repository foundation.** The analytical methods, data strategy, and
dashboard choice are being finalized before data is acquired or generated.

## Repository structure

```text
.
├── config/                 # Non-secret pipeline and model configuration
├── dashboard/              # Interactive dashboard application and assets
├── data/
│   ├── external/           # Third-party source data (not committed)
│   ├── interim/            # Reproducible intermediate outputs (not committed)
│   ├── processed/          # Analysis-ready outputs (not committed)
│   ├── raw/                # Immutable simulated/source exports (not committed)
│   └── sample/             # Small, safe fixtures that may be committed
├── docs/                   # Charter, dictionary, decisions, and methodology
├── notebooks/              # Numbered, narrative analysis notebooks
├── reports/
│   ├── figures/            # Publication-ready visualizations
│   └── tables/             # Final analytical tables
├── scripts/                # Reproducible command-line entry points
├── sql/
│   ├── analyses/           # Business questions and validation queries
│   ├── intermediate/       # Reusable transformations
│   ├── marts/              # Customer, retention, catalog, and movie marts
│   └── staging/            # Source cleaning and type normalization
├── src/vod_retention/      # Tested Python package
└── tests/                  # Unit and data-quality tests
```

Each top-level directory contains local guidance describing what belongs there.

## Working principles

- Separate observed data, simulated data, estimates, assumptions, and proposed experiments.
- Keep raw inputs immutable and make every downstream artifact reproducible.
- Use SQL for analytical transformations and Python for validation, statistics,
  scoring, and visualization.
- Prefer explainable methods and chronological evaluation over unnecessary model complexity.
- Never commit credentials, personal data, or large third-party datasets.

## Local setup

Python 3.11 or later is recommended.

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -e ".[dev]"
```

Run the repository checks with:

```bash
make check
```

Data acquisition commands will be added after the data-source decision is
recorded. Raw data will be downloaded or generated locally rather than stored in
Git.

## Planned deliverables

1. Reproducible data model and data-quality checks
2. Defensible power-user and behavioral-churn definitions
3. Catalog-exhaustion analysis with limitations and sensitivity tests
4. Explainable candidate scoring and a constrained 1,000-title portfolio
5. Chronological offline evaluation against multiple baselines
6. Interactive dashboard, experiment plan, and portfolio-ready communication

## License

Original code and documentation are available under the [MIT License](LICENSE).
Third-party datasets remain subject to their respective terms and are not
covered by this repository's license.
