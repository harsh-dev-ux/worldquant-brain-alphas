# Alpha 006 — Income–Volume Blend

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor (Profitability Yield + Volume-Price Dynamics) |
| **Data Fields** | Operating income, Total equity, Volume-price ratio series, Close prices |
| **Technique** | Multi-level hierarchical group ranking across subindustry and industry classifications |
| **Lookback** | 126 trading days (~6 months) |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 40 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.91 |
| Fitness | 4.77 |
| Turnover | 6.91% |
| Self-Correlation (Max) | 0.6373 |
| Self-Correlation (Min) | −0.0697 |

## Intuition

> Leverages dual-horizon factor weighting combining operating earnings efficiency with volume-adjusted price trends, mitigating sector concentration.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
