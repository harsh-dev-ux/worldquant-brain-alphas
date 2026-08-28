# Alpha 002 — SCL12 Sentiment

**Status:** Accepted
**Created on BRAIN:** 2026-08-17

---

## Formula

```
group_neutralize(scl12_buzz, bucket(rank(volume), range(0.1, 0.1)))
```

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

## Logic

> Isolates social sentiment signal from liquidity effects by neutralizing SCL12 buzz scores across volume-based decile buckets.

---

*Documented as part of [worldquant-brain-alphas](../README.md)*
