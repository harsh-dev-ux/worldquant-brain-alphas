# Alpha 003 — Operating Income Rank

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Fundamental Quality & Profitability |
| **Data Fields** | Operating income, Market capitalization |
| **Technique** | Time-series ranking of profitability-to-market size yield |
| **Lookback** | 252 trading days (~1 year) |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP1000 |
| Decay | 8 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.51 |
| Fitness | 1.28 |
| Turnover | 8.09% |
| Self-Correlation (Max) | 0.6373 |
| Self-Correlation (Min) | −0.0822 |

## Intuition

> Identifies companies with sustained operating earnings yield relative to their historical baseline, harvesting low-turnover fundamental re-rating alpha.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
