# Alpha 013 — Volume-Surge Short-Term Mean Reversion

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Price-Volume Interaction / Short-Term Mean Reversion |
| **Data Fields** | Closing prices, Daily trading volume |
| **Technique** | Inverse short-term price delta weighted by abnormal volume surge relative to baseline |
| **Lookback** | 2-day price reversion conditioned on 30-day volume moving average |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
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
| Sharpe | 2.03 |
| Fitness | 1.07 |
| Turnover | 48.70% |
| Returns | 13.52% |
| Margin | 5.54 bps |
| Self-Correlation (Max) | 0.5458 |
| Self-Correlation (Min) | −0.0885 |

## Intuition

> Targets liquidity-driven capitulation events: identifies equities experiencing sharp 2-day price declines coupled with anomalous volume spikes relative to their 30-day baseline, positioning for immediate mean-reverting liquidity relief bounces.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
