# Alpha 002 — SCL12 Sentiment

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Alternative Data / Social Sentiment & Liquidity Interaction |
| **Data Fields** | SCL12 social sentiment & buzz metrics, Trading volume |
| **Technique** | Non-linear volume decile bucketing and group neutralization |
| **Lookback** | Intraday social buzz signal neutralized across discrete volume buckets |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 6 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Industry |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 2.15 |
| Fitness | 1.51 |
| Turnover | 60.57% |
| Self-Correlation (Max) | 0.1239 |
| Self-Correlation (Min) | −0.0822 |

## Intuition

> Isolates authentic crowd sentiment by conditioning buzz metrics across volume liquidity buckets, stripping out noise from mega-cap retail attention.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
