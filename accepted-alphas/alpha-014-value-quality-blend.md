# Alpha 014 — Value & Operating Quality Dual-Horizon Blend

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor (Fundamental Value + Operating Capital Quality) |
| **Data Fields** | Total Common Equity, Market Capitalization, Operating Income |
| **Technique** | Dual-horizon factor ranking combining short-term book-to-market yield with medium-term operating ROE across nested subindustry/industry tiers |
| **Lookback** | 20-day time-series rank for valuation yield + 126-day time-series rank for operating profitability |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 5 |
| Delay | 1 |
| Truncation | 0.05 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 2.65 |
| Fitness | 2.05 |
| Turnover | 19.79% |
| Returns | 11.82% |
| Margin | 11.96 bps |
| Self-Correlation (Max) | 0.5691 |
| Self-Correlation (Min) | −0.0466 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 3.08 | 20.31% | 1.94 | 8.08% | 1.84% | 7.96 bps |
| 2020 | 2.99 | 20.31% | 2.56 | 14.94% | 2.99% | 14.71 bps |
| 2021 | 2.26 | 18.75% | 1.85 | 12.50% | 2.82% | 13.33 bps |
| 2022 | 2.72 | 19.65% | 2.33 | 14.39% | 2.24% | 14.65 bps |
| 2023 | 2.85 | 19.89% | 1.97 | 9.49% | 1.99% | 9.54 bps |

## Intuition

> Systematic implementation of Quality at a Reasonable Price (QARP): dynamically screens for attractive valuation multiples (book-to-market) while conditioning strictly on positive operating profitability (ROE), effectively purging classical value traps while delivering remarkable year-over-year Sharpe stability (Sharpe > 2.2 across every backtested year).

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
