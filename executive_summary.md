# Executive Summary

This historical analysis supports exploratory research by financial analysts.

## Findings
1. The file contains 497,472 rows, 505 symbols and 1,007 dates (2014-01-02 to 2017-12-29).
2. Five-stock comparison uses 1,007 common dates.
3. Highest common-period return: AMZN (193.9%); lowest: XOM (-16.2%).
4. Highest annualized volatility: AMZN (29.6%); lowest: XOM (17.9%).
5. The highest raw close was PCLN at 2049.00; raw close is not return performance.
6. Open/high/low missing counts are 11/8/8; zero-volume observations: 4.
7. 26 symbols have fewer than 1,007 distinct dates.
8. 39 absolute one-day returns exceed 25%; flagged for verification, not removed.

## Recommendations
1. Compare stocks by common-date percentage returns, not raw close alone; this period ranges from XOM at -16.2% to AMZN at +193.9%, while their nominal share prices differ greatly.
2. Review exceptional returns and OHLC flags against adjusted prices and corporate-action data before risk use; 39 daily returns exceed ±25% and 12 complete rows breach OHLC bounds.
3. Use the dashboard for descriptive research only; it shows distinct selected-stock returns and volatility but has no out-of-sample predictive validation.
4. Repeat key, null, OHLC, volume and coverage checks on refresh; the source has 26 symbols with incomplete date coverage and four zero-volume rows.

## Limitations
2014-2017 only; no adjusted close, verified corporate actions, explicit currency, or full constituent timeline. Volume is shares traded. Not investment advice; history is not a forecast.
