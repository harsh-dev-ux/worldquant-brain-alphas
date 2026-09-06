# Alpha 016 — Options Surface Put Pressure Ratio

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Derivatives / Options Implied Volatility Surface |
| **Data Fields** | 120-Day Call Implied Volatility, 120-Day Put Implied Volatility |
| **Technique** | Relative put implied volatility pressure ratio against total surface volatility with 5-day time-series backfill for sparse option reporting |
| **Lookback** | 5-day backfill on 120-day constant-maturity implied volatility term structures |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 12 |
| Delay | 1 |
| Truncation | 0.01 |
| Neutralization | None |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.56 |
| Fitness | 1.48 |
| Turnover | 9.98% |
| Returns | 11.21% |
| Margin | 22.46 bps |
| Self-Correlation (Max) | 0.6995 |
| Self-Correlation (Min) | 0.0650 |

### Out-of-Sample Yearly Breakdown

| Year | Sharpe | Turnover | Fitness | Returns | Drawdown | Margin |
|------|--------|----------|---------|---------|----------|--------|
| 2019 | 2.30 | 8.44% | 2.33 | 11.77% | 2.64% | 27.91 bps |
| 2020 | 0.86 | 10.63% | 0.39 | 4.94% | 13.00% | 9.30 bps |
| 2021 | 2.03 | 9.76% | 2.18 | 14.41% | 7.81% | 29.57 bps |
| 2022 | 2.36 | 12.82% | 2.75 | 17.43% | 7.00% | 27.20 bps |
| 2023 | 1.59 | 8.25% | 1.20 | 7.10% | 3.04% | 16.99 bps |

## Intuition

> Quantifies institutional hedging demand and downside tail-risk pricing across the 120-day options maturity surface. By measuring the proportion of total implied volatility attributable to put contracts relative to call contracts (`put / (call + put)`), the signal isolates persistent variance risk premia and institutional hedging pressure across broad-market equities, generating robust out-of-sample risk-adjusted returns (OS Sharpe 1.56, Margin 22.46 bps) with low portfolio turnover (~10%).

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
