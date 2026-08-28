# Alpha 003 — Operating Income Rank

**Status:** Accepted
**Created on BRAIN:** 2026-08-25

---

## Formula

```
ts_rank(operating_income / cap, 252)
```

## Settings

| Parameter | Value |
|-----------|-------|
| Region | USA |
| Universe | TOP1000 |
| Decay | 8 |
| Delay | 1 |
| Truncation | 0.08 |
| Neutralization | Subindustry |
| Pasteurization | On |
| NaN Handling | Off |
| Unit Handling | Verify |

## Performance (OS)

| Metric | Value |
|--------|-------|
| Sharpe | 1.51 |
| Fitness | 1.28 |
| Turnover | 8.09% |
| Self-Correlation (Max) | 0.6373 |
| Self-Correlation (Min) | −0.0822 |

## Logic

> Ranks stocks by operating profitability relative to market cap over a 252-day lookback, capturing persistent fundamental value with low turnover.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
