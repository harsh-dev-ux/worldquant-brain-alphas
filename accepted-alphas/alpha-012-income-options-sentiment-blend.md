# Alpha 012 — Operating Income & Options Sentiment Blend

---

## Approach

| Component | Description |
|-----------|-------------|
| **Signal Type** | Multi-Factor (Fundamental Profitability + Options Positioning Sentiment) |
| **Data Fields** | Operating Income, Total Equity, Options Put-Call Open Interest (`pcr_oi_220`) |
| **Technique** | Dual-factor ranking combining fundamental operating return on equity with inverse put-call open interest sentiment rank |
| **Lookback** | 126-day fundamental rank combined with 120-day options positioning rank |

> 🔒 *Formula available on request — DM on LinkedIn.*

---

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 20 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | On |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 2.28 |
| Fitness | 1.71 |
| Turnover | 5.20% |
| Returns | 7.07% |
| Margin | 28.67 bps |
| Self-Correlation (Max) | 0.3325 |
| Self-Correlation (Min) | −0.1066 |

## Intuition

> Pairs fundamental quality with institutional options positioning: allocates capital to profitable businesses where bearish options hedging/put open interest is diminishing, generating high risk-adjusted performance (2.28 Sharpe, 28.67 bps margin) with minimal turnover (5.2%).

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
