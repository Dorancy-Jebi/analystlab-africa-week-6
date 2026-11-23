# Data-quality assessment

Rows 497,472; 7 columns; 505 symbols; 1007 distinct dates; 2014-01-02 to 2017-12-29.

| Check | Result | Decision |
|---|---:|---|
| Missing open/high/low/close | 11/8/8/0 | Retain nulls; no zero imputation. |
| Duplicate symbol-date keys | 0 | Key uniqueness checked. |
| Zero volume | 4 | Retain and flag. |
| Incomplete histories | 26/505 symbols | Coverage exported; selected comparison uses shared dates. |
| OHLC bounds violations (complete rows) | 12 | Diagnostic; row-level flags in `ohlc_bound_violations.csv`; no silent edits. |
| Return magnitude greater than 25% | 39 | Flagged but retained pending source verification. |

Dates are parsed and sorted by symbol. Derived fields are year, month, quarter, close change, percentage return, high-low range and per-symbol 20/50-session simple moving averages. `pct_change(fill_method=None)` avoids implicit filling; moving averages require full windows.

No adjusted close, corporate-action history, currency metadata or constituent membership history is supplied. Do not assume all 505 symbols were continuous index members.
