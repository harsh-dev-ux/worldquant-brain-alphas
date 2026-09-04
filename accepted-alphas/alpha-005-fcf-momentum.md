# Alpha 005 — FCF + Momentum

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor (Fundamental Cash Flow + Price Momentum) |
| **Data Fields** | Free cash flow reported value, Total equity, Close prices |
| **Technique** | Two-factor rank blending with industry group normalization |
| **Lookback** | 126-day fundamental rank combined with 5-day delta momentum |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP1000 |
| Decay | 10 |
| Delay | 1 |
| Truncation | 0.05 |
| Neutralization | Industry |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.60 |
| Fitness | 1.21 |
| Turnover | 7.07% |
| Self-Correlation (Max) | 0.3734 |
| Self-Correlation (Min) | 0.0702 |

## Intuition

> Combines medium-term cash flow generation quality with short-term price momentum, selecting companies with both valuation support and price confirmation.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
