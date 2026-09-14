# Alpha 023 — CFF Flag & Leverage Rank

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Cash Flow Flag & Balance Sheet Leverage |
| **Data Fields** | ANL4 Cash Flow Flag, Total Assets, Current Liabilities |
| **Technique** | Cross-sectional ranking of cash flow signal against assets-to-current-liabilities leverage ratio |
| **Decay / Delay** | 1 / 1 |

> *Exact expression withheld while the signal remains active.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
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
| Sharpe | 1.85 |
| Fitness | 2.19 |
| Turnover | 2.11% |
| Returns | 17.57% |
| Margin | 166.86 bps |
| Self-Correlation (Max) | 0.3474 |
| Self-Correlation (Min) | -0.1065 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 1.08 | 2.42% | 0.82 | 7.29% | 7.19% | 60.17 bps |
| 2020 | 2.12 | 2.15% | 2.89 | 23.26% | 7.55% | 216.53 bps |
| 2021 | 2.99 | 2.05% | 4.83 | 32.60% | 5.98% | 318.27 bps |
| 2022 | 1.41 | 1.99% | 1.56 | 15.21% | 6.64% | 152.74 bps |
| 2023 | 1.41 | 1.93% | 1.28 | 10.29% | 4.14% | 106.69 bps |

## Intuition

> Contrasts a proprietary cash flow classification flag against a simple balance sheet leverage ratio (assets ÷ current liabilities). Stocks with favorable cash flow flags but low leverage ratio rank highest, capturing quality-adjusted balance sheet strength with minimal turnover.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
