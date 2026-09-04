# Alpha 009 — Consensus Net Profit Earnings Yield

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Fundamental / Analyst Consensus & Forward Earnings Yield |
| **Data Fields** | Analyst consensus net profit mean estimates, Market Capitalization |
| **Technique** | Time-series backfilled consensus yield, statistical outlier winsorization (4.0 std), and cross-sectional industry z-score |
| **Lookback** | 40-day smoothed forward consensus earnings yield |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 15 |
| Delay | 1 |
| Truncation | 0.01 |
| Neutralization | None |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.46 |
| Fitness | 1.43 |
| Turnover | 4.51% |
| Returns | 12.01% |
| Margin | 33.29 bps |
| Self-Correlation (Max) | 0.2065 |
| Self-Correlation (Min) | −0.1025 |

## Intuition

> Exploits persistent post-revision drift by standardizing forward-looking analyst net profit estimates relative to firm valuation, winsorizing extreme outliers to avoid distress bias and standardizing within industry peer groups.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
