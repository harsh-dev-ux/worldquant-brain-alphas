# Alpha 006 — Income–Volume Blend

**Status:** Accepted
**Created on BRAIN:** 2026-08-28

---

## Formula

```
a = 0.5 * group_rank(ts_rank(operating_income / equity, 126), subindustry)
b = 0.5 * group_rank(ts_rank(vt_1 / close, 126), industry)
```

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

## Logic

> Equally-weighted blend of operating income yield and a volume-price ratio signal, each ranked within subindustry and industry respectively over a 126-day window.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
