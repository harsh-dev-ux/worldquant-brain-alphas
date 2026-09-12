# Alpha 019 — Large-Cap Operating ROE & Cash Yield Dual-Factor Blend

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor (Operating Profitability + Cash Flow Yield) |
| **Data Fields** | Operating Income, Common Equity, Operating Cash Flow (`cashflow_op`), Market Capitalization |
| **Technique** | Equal-weighted blend of two group-ranked time-series signals: 126-day operating ROE (`operating_income / equity`) ranked within industry groups, and 60-day operating cash yield (`cashflow_op / cap`) ranked within subindustry peers |
| **Lookback** | 126-day time-series rank for operating ROE + 60-day time-series rank for cash yield |

> *Exact expression withheld while the signal remains active.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP500 |
| Decay | 5 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.61 |
| Fitness | 1.16 |
| Turnover | 16.11% |
| Returns | 8.39% |
| Margin | 10.65 bps |
| Self-Correlation (Max) | 0.5043 |
| Self-Correlation (Min) | 0.0570 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 1.23 | 15.09% | 0.74 | 4.90% | 3.13% | 5.20 bps |
| 2020 | 2.64 | 17.74% | 2.51 | 15.44% | 3.71% | 16.01 bps |
| 2021 | 1.07 | 15.02% | 1.20 | 11.24% | 4.02% | 11.40 bps |
| 2022 | 1.60 | 15.74% | 0.61 | 5.61% | 3.21% | 7.19 bps |
| 2023 | 1.21 | 16.24% | 0.69 | 5.21% | 3.50% | 5.32 bps |

## Intuition

> A dual-factor QARP variant focused on the large-cap TOP500 universe, combining medium-term operating ROE momentum (126-day `group_rank` within industry) with short-term cash yield momentum (60-day `group_rank` within subindustry). By splitting normalization tiers — industry for the longer ROE signal and subindustry for the shorter cash yield signal — the alpha captures profitability alpha at different levels of peer granularity simultaneously. The equal-weight (0.5/0.5) blend provides consistent risk-adjusted performance across market regimes (Sharpe consistently above 1.0 across all five OS years), with standout 2020 Sharpe of 2.64.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
