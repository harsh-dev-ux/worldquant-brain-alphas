# Alpha 015 — Large-Cap Value & Quality Dual-Horizon Blend

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor (Fundamental Value + Operating Capital Quality) |
| **Data Fields** | Total Common Equity, Market Capitalization, Operating Income |
| **Technique** | Dual-horizon factor ranking combining short-term book-to-market yield with medium-term operating ROE across nested subindustry/industry tiers in large-cap equities |
| **Lookback** | 20-day time-series rank for valuation yield + 126-day time-series rank for operating profitability |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP500 |
| Decay | 5 |
| Delay | 1 |
| Truncation | 0.05 |
| Neutralization | Industry |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.58 |
| Fitness | 1.03 |
| Turnover | 20.36% |
| Returns | 8.60% |
| Margin | 8.45 bps |
| Self-Correlation (Max) | 0.5841 |
| Self-Correlation (Min) | −0.0592 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 1.77 | 20.50% | 0.90 | 5.35% | 2.58% | 5.22 bps |
| 2020 | 2.03 | 20.64% | 1.53 | 11.74% | 4.50% | 11.38 bps |
| 2021 | 1.86 | 20.21% | 1.51 | 13.33% | 3.94% | 13.19 bps |
| 2022 | 1.91 | 20.18% | 1.42 | 11.21% | 3.86% | 11.12 bps |
| 2023 | 0.38 | 20.29% | 0.11 | 1.71% | 4.44% | 1.69 bps |

## Intuition

> Large-cap (TOP500) adaptation of the Quality at a Reasonable Price (QARP) framework. Focuses on the most liquid equity universe by pairing short-term valuation multiple rankings (book-to-market) with medium-term operating profitability (ROE), neutralized across broader industry groups to capture persistent fundamental alpha in institutional-grade equities.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
