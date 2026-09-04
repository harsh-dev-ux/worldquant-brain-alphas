# Alpha 001 — Market Microstructure

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Market Microstructure & Conditional Momentum |
| **Data Fields** | Trade imbalance indicators, Volume distribution, Close price |
| **Technique** | Vector imbalance aggregation gating short-term price momentum |
| **Lookback** | Multi-day volume imbalance condition with short-term price delta |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP1000 |
| Decay | 23 |
| Delay | 1 |
| Truncation | 0.01 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.77 |
| Fitness | 1.68 |
| Turnover | 8.81% |
| Self-Correlation (Max) | 0.3734 |
| Self-Correlation (Min) | 0.0342 |

## Intuition

> Uses market microstructure order flow and volume imbalance to gate short-term momentum — allocating only when directional institutional flow confirms the move.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
