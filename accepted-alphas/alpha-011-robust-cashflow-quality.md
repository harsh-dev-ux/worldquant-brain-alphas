# Alpha 011 — Robust Cash Flow Quality

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Fundamental Quality / Robust Cash Generation |
| **Data Fields** | Operating Cash Flow (`cashflow_op`), Market Capitalization |
| **Technique** | Intermediate factor structuring, time-series ranking, and subindustry ranking with missing data imputation |
| **Lookback** | 60-day historical time-series rank |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 4 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 2.14 |
| Fitness | 1.60 |
| Turnover | 17.07% |
| Returns | 9.31% |
| Margin | 11.14 bps |
| Self-Correlation (Max) | 0.9361 |
| Self-Correlation (Min) | 0.0722 |

## Intuition

> Refined cash generation alpha utilizing robust missing data handling to preserve coverage across broader universe constituents, capturing superior risk-adjusted returns (2.14 Sharpe) through cleaner cross-sectional subindustry distribution.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
