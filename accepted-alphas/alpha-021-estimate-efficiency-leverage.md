# Alpha 021 — Estimate Efficiency & Leverage Blend

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor (Capital Efficiency + Analyst Estimates + Balance-Sheet Leverage) |
| **Data Fields** | EBIT, CAPEX, Operating Income, Estimated EPS, Estimated Net Profit, Close Price, Total Liabilities, Total Assets |
| **Technique** | Long-horizon capital efficiency rank blended with consensus estimate-yield composite, scaled by balance-sheet leverage |
| **Lookback** | 504-day time-series rank for efficiency component + 252-day time-series rank for estimate components |

> *Exact expression withheld while the signal remains active.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP500 |
| Decay | 1 |
| Delay | 1 |
| Truncation | 0.01 |
| Neutralization | Market |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |
| Max Trade | Off |
| Max Position | Off |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.59 |
| Fitness | 1.69 |
| Turnover | 13.34% |
| Returns | 15.13% |
| Margin | 22.69 bps |
| Self-Correlation (Max) | 0.6211 |
| Self-Correlation (Min) | 0.0342 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 2.02 | 13.67% | 1.90 | 12.05% | 4.58% | 17.63 bps |
| 2020 | 1.36 | 14.63% | 1.55 | 18.95% | 8.58% | 25.90 bps |
| 2021 | 2.79 | 13.09% | 3.84 | 24.74% | 5.31% | 37.82 bps |
| 2022 | 2.19 | 13.69% | 2.73 | 21.32% | 4.46% | 31.15 bps |
| 2023 | -0.22 | 11.72% | -0.08 | -1.71% | 7.96% | -2.93 bps |

## Intuition

> Combines capital deployment efficiency with forward-looking analyst expectations, amplified by leverage exposure. Rewards firms that convert investment efficiently while screening on consensus earnings strength, with market neutralization isolating stock-specific quality dispersion in large caps.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
