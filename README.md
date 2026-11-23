# Week 6 - Data Analytics

Contents: completed notebook, Python preparation script, four-section Plotly dashboard, KPI definitions, data-quality assessment, executive summary, CSV analysis outputs, validation evidence and four dashboard page previews in `evidence/dashboard_previews/`. The previews are static renders from the analysis data, not browser screenshots. Source snapshot is in `data/source_copy.csv`.

Reproduce with Python 3.10+, pandas, numpy and reportlab: `python scripts/prepare_analyze.py [source.csv]`. Default input is the bundled source copy. Dashboard needs internet for Plotly CDN.

Five selected symbols are AAPL, MSFT, AMZN, GOOGL and XOM. Returns and moving averages are grouped per symbol after sorting. The comparison uses shared dates. Annualized sample volatility uses sqrt(252). Missing values stay missing. Validation rows are in `evidence/validation_checks.csv`.

Limitations: historical 2014-2017 only; no adjusted close, corporate action verification, explicit currency or complete constituent history. Historical returns are not advice or guarantees. Rename the folder to include your full name before submission.
