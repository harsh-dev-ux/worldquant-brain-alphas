# Alpha 004 — Volatility Skew

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Derivatives / Options Implied Volatility Surface |
| **Data Fields** | Implied volatility call & put surfaces |
| **Technique** | Backfilled call-put surface spread, cross-sectional industry z-score |
| **Lookback** | Time-series backfill & smoothing with cross-sectional normalization |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 22 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | None |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.91 |
| Fitness | 3.12 |
| Turnover | 4.77% |
| Self-Correlation (Max) | 0.2064 |
| Self-Correlation (Min) | 0.0852 |

## Intuition

> Exploits pricing asymmetries between call and put implied volatility surfaces, standardizing signals across industry peers to capture volatility risk premia.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
