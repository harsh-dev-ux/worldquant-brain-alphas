# Alpha 020 - Large-Cap Operating Profitability Blend

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor Fundamental Quality / Operating Profitability |
| **Data Fields** | Operating Income, Common Equity, proprietary supporting inputs |
| **Technique** | Weighted profitability construction using a long-horizon operating-income-to-equity signal normalized within industry peers |
| **Lookback** | 252-day time-series rank on the visible operating profitability component |

> *Exact expression withheld while the signal remains active.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP500 |
| Decay | 3 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Market |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |
| Max Trade | Off |
| Max Position | Off |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.52 |
| Fitness | 1.23 |
| Turnover | 11.26% |
| Returns | 8.13% |
| Margin | 14.44 bps |
| Self-Correlation (Max) | 0.6175 |
| Self-Correlation (Min) | 0.0235 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 0.76 | 11.22% | 0.33 | 2.40% | 3.48% | 4.28 bps |
| 2020 | 2.03 | 12.11% | 2.04 | 12.66% | 5.96% | 20.91 bps |
| 2021 | 1.40 | 11.06% | 1.22 | 9.50% | 6.85% | 17.18 bps |
| 2022 | 2.59 | 11.12% | 2.77 | 14.32% | 2.53% | 25.75 bps |
| 2023 | 0.63 | 10.89% | 0.29 | 2.68% | 4.27% | 4.92 bps |

## Intuition

> Focuses on large-cap companies whose operating profitability is strong relative to their equity base, measured against the firm's own history and normalized across industry peers. Market neutralization removes broad market exposure, while the weighted construction targets stock-specific quality dispersion with controlled turnover.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
