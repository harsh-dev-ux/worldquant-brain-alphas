# Alpha 007 — Mean Reversion + Financial Leverage

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor (Short-Term Mean Reversion + Capital Structure Leverage) |
| **Data Fields** | Closing prices, Total Debt, Enterprise Value |
| **Technique** | Inverse moving average divergence blended with debt-to-EV cross-sectional rank |
| **Lookback** | 10-day price average difference combined with balance sheet leverage |

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
| Neutralization | Industry |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.40 |
| Fitness | 1.32 |
| Turnover | 21.77% |
| Returns | 17.29% |
| Margin | 15.89 bps |
| Self-Correlation (Max) | 0.4245 |
| Self-Correlation (Min) | 0.0226 |

## Intuition

> Combines a short-term 10-day price mean-reversion component with capital structure leverage (debt / enterprise value), identifying oversold equities with high operating/financial leverage that exhibit pronounced mean-reverting recoveries.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
