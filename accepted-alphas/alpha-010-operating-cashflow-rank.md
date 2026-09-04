# Alpha 010 — Operating Cash Flow Yield Rank

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Fundamental Quality & Cash Flow Generation |
| **Data Fields** | Operating Cash Flow (`cashflow_op`), Market Capitalization |
| **Technique** | Time-series ranking of cash flow yield with cross-sectional subindustry group ranking |
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
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.84 |
| Fitness | 1.22 |
| Turnover | 18.50% |
| Returns | 8.11% |
| Margin | 8.77 bps |
| Self-Correlation (Max) | 0.9361 |
| Self-Correlation (Min) | −0.0521 |

## Intuition

> Identifies equities experiencing cash flow yield improvements relative to recent history, grouping by subindustry to neutralize structural sector cash conversion disparities.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
