# Alpha 022 — Operating Income Quantile Yield

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Fundamental Quality / Operating Profitability Yield |
| **Data Fields** | Operating Income, Market Capitalization |
| **Technique** | Time-series quantile ranking of operating profitability-to-size ratio with cross-sectional ranking |
| **Lookback** | 120-day time-series quantile window |

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
| Sharpe | 1.74 |
| Fitness | 1.55 |
| Turnover | 18.92% |
| Returns | 14.98% |
| Margin | 15.83 bps |
| Self-Correlation (Max) | 0.5949 |
| Self-Correlation (Min) | -0.0846 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 3.19 | 19.21% | 2.93 | 16.23% | 2.98% | 16.89 bps |
| 2020 | 2.26 | 20.03% | 2.52 | 24.98% | 6.21% | 24.94 bps |
| 2021 | 1.78 | 18.35% | 1.58 | 14.52% | 3.99% | 15.82 bps |
| 2022 | 1.54 | 19.18% | 1.45 | 16.93% | 5.23% | 17.66 bps |
| 2023 | 0.59 | 17.97% | 0.27 | 3.68% | 6.19% | 4.10 bps |

## Intuition

> Ranks large-cap stocks by where current operating profitability relative to market cap sits in its own 120-day history. Market neutralization isolates stock-specific quality momentum with controlled turnover.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
