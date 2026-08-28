# Alpha 004 — Volatility Skew

**Status:** Accepted
**Created on BRAIN:** 2026-08-25

---

## Formula

```
cl04 = ts_backfill(implied_volatility_call_1m, 5);
pl04 = ts_backfill(implied_volatility_put_04m, 5);
skew = (cl04 - pl04);
group_zscore(ts_mean(skew, all), industry)
```

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP3000 |
| Decay | 22 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | None |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.91 |
| Fitness | 3.12 |
| Turnover | 4.77% |
| Self-Correlation (Max) | 0.2064 |
| Self-Correlation (Min) | 0.0852 |

## Logic

> Captures options-implied volatility skew between call and put surfaces, z-scored within industries to isolate relative mispricing in the volatility term structure.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
