# Alpha 005 — FCF + Momentum

**Status:** Accepted
**Created on BRAIN:** 2026-08-27

---

## Formula

```
a = group_rank(ts_rank(free_cash_flow_reported_value / equity, 126), industry)
b = group_rank(ts_delta(close, 5), industry)
```

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

## Logic

> Blends fundamental free cash flow yield rank with short-term 5-day price momentum, both ranked within industry groups to capture value-momentum convergence.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
