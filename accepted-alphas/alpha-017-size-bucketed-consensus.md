# Alpha 017 — Market-Cap Stratified Analyst Consensus & Sentiment

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Alternative / Analyst Consensus & Broker Sentiment |
| **Data Fields** | Broker Sentiment Indicator (`pv13`), Market Capitalization (`cap`), Analyst Consensus Revisions (`pv15`) |
| **Technique** | Market-capitalization decile bucketing interacting with 120-day time-series backfilled analyst consensus revisions and broker sentiment signals |
| **Lookback** | 120-day time-series backfill on analyst consensus estimates |

> *Exact expression withheld while the signal remains active.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 0 |
| Delay | 1 |
| Truncation | 0.02 |
| Neutralization | None |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.35 |
| Fitness | 1.26 |
| Turnover | 9.37% |
| Returns | 8.23% |
| Margin | 17.55 bps |
| Self-Correlation (Max) | 0.4795 |
| Self-Correlation (Min) | −0.0600 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 1.35 | 9.41% | 0.91 | 5.64% | 4.28% | 11.98 bps |
| 2020 | 1.36 | 9.55% | 1.17 | 9.30% | 2.90% | 19.46 bps |
| 2021 | 2.01 | 9.64% | 2.17 | 15.30% | 2.82% | 32.01 bps |
| 2022 | 2.20 | 9.15% | 2.07 | 11.11% | 2.00% | 24.29 bps |
| 2023 | -0.19 | 9.13% | -0.05 | -0.88% | 5.47% | -1.92 bps |

## Intuition

> Stratifies analyst consensus recommendations and revisions across size deciles using non-linear capitalization bucketing (`bucket(rank(cap))`). Standardizing broker sentiment signals within homogenous market-cap cohorts captures institutional information diffusion and revision drift while mitigating large-cap bias, sustaining low portfolio turnover (<10%) and robust execution margin (17.55 bps) across the broad-market TOP3000 universe.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
