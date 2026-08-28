# Research Notes

Notes and takeaways from building alphas on WorldQuant BRAIN.

---

## General Principles

- **Low self-correlation matters.** Alphas that are too autocorrelated get flagged. Decay and truncation tuning are key levers.
- **Neutralization is not optional.** Industry or subindustry neutralization removes sector beta and makes the signal purer. Without it, you're mostly trading sector momentum.
- **Turnover is a constraint, not just a metric.** High-turnover alphas eat into margin. The scl12 sentiment alpha runs ~60% turnover — it passed, but it's near the edge.
- **Fundamentals are robust but slow.** Operating income, FCF, and equity-based signals are stable across years but need longer lookbacks (126–252 days) to generate meaningful rank dispersion.

## What Worked

- **Bucketing volume before neutralizing sentiment** (Alpha 002) was the key insight for the scl12 alpha. Raw sentiment is noisy; conditioning on liquidity regime cleaned it up significantly.
- **Mixing fundamental + momentum factors** (Alphas 005, 006) consistently produces better fitness than either factor alone. The group_rank within industry/subindustry is important — raw ranks leak sector exposure.
- **Options volatility skew** (Alpha 004) is an underexplored data source on BRAIN. The call-put implied vol spread carries real signal, especially when z-scored.

## What Didn't Work

- Raw price momentum without any fundamental gating — high Sharpe in-sample, collapses out-of-sample.
- Overfitting decay parameters. Started by grid-searching decay values; learned to pick a reasonable value (5–20 for most alphas) and focus on the expression instead.
- Single-factor alphas on overcrowded fields (e.g., plain `rank(close/open)`) — too many existing alphas in those spaces, self-correlation kills them.

## Platform Notes

- Fast Expression language is sufficient for most alpha research. No need for the full expression engine unless you're doing complex multi-line logic.
- TOP3000 universe is harder to get accepted in (more competition) but the margin tends to be higher.
- TOP1000 is good for cleaner fundamentals since data quality is better for large caps.

---

*Continuously updated as research progresses.*
