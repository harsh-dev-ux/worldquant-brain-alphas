# Alpha 008 — Implied vs Parkinson Volatility Ratio

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Volatility Surface Arbitrage / Variance Risk Premium |
| **Data Fields** | Options implied volatility call surface (120d), Parkinson realized volatility (120d) |
| **Technique** | Forward-looking implied volatility normalized against historical high-low price range volatility |
| **Lookback** | 120-day implied-to-realized volatility term structure, backfilled |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP200 |
| Decay | 0 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Sector |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.39 |
| Fitness | 1.48 |
| Turnover | 21.52% |
| Returns | 24.52% |
| Margin | 22.79 bps |
| Self-Correlation (Max) | 0.2264 |
| Self-Correlation (Min) | −0.2148 |

## Intuition

> Quantifies the volatility risk premium by comparing forward-looking options implied volatility against empirical high-low Parkinson price volatility, systematically harvesting pricing discrepancies across the most liquid large-cap equities.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
