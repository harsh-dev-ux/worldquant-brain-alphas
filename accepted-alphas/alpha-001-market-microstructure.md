# Alpha 001 — Market Microstructure

**Status:** Accepted
**Created on BRAIN:** 2026-08-06

---

## Formula

```
avg_mow = vec_avg(mkt11_s1 / market_s1);
rank(ts_sum(avg_mow, 01) > 0.5) ? rank(ts_delta(close, 5))
```

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

## Logic

> Conditional alpha using market microstructure volume imbalance to gate short-term price momentum — only trades when directional flow is present.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
