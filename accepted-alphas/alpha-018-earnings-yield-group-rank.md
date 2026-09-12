# Alpha 018 — Earnings Yield Rank with Subindustry Group Normalization

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Fundamental / Earnings Yield Momentum |
| **Data Fields** | Net EPS (`net_eps`), Closing Price (`close`) |
| **Technique** | 252-day time-series rank of trailing EPS yield (`net_eps / close`), then cross-sectionally grouped and ranked within subindustry peers using `group_rank` |
| **Lookback** | 252-day rolling time-series rank on earnings yield |

> *Exact expression withheld while the signal remains active.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 0 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.69 |
| Fitness | 1.38 |
| Turnover | 18.24% |
| Returns | 8.50% |
| Margin | 6.38 bps |
| Self-Correlation (Max) | 0.6546 |
| Self-Correlation (Min) | 0.0505 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 0.33 | 17.30% | 0.34 | 2.25% | 5.26% | 3.24 bps |
| 2020 | 0.55 | 19.67% | 0.86 | 13.17% | 7.16% | 17.48 bps |
| 2021 | 2.52 | 17.52% | 1.30 | 10.23% | 2.76% | 11.75 bps |
| 2022 | 3.14 | 19.71% | 1.41 | 8.87% | 9.84% | 9.45 bps |
| 2023 | 0.31 | 14.41% | 0.30 | 2.07% | 2.92% | 3.62 bps |

## Intuition

> Constructs a two-stage earnings yield signal: first, time-series ranking (`ts_rank`) of each stock's EPS yield over 252 days to capture the trajectory of earnings improvement relative to its own history; second, `group_rank` within subindustry peers to neutralize sector-level EPS cycles and isolate idiosyncratic valuation trends. The construction rewards companies demonstrating persistently rising earnings yield relative to their immediate competitive set, with notably strong Sharpe in 2021–2022 (2.52 and 3.14 respectively).

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
