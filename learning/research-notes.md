# Research Notes

Notes and takeaways from building quantitative alphas on WorldQuant BRAIN.

---

## General Principles

- **Low self-correlation is paramount.** Alphas that overlap with crowded factors get penalized. Decay, neutralization, and factor blending are key levers to compress correlation below 0.35.
- **Neutralization is essential.** Subindustry and industry neutralization removes market and sector beta, ensuring you isolate pure idiosyncratic alpha rather than unintended factor bets.
- **Turnover is a hard constraint.** High-turnover signals degrade rapidly when factoring in transaction costs and slippage. Keeping turnover under 20% preserves margin.
- **Fundamental and alternative data synergy.** Pure price momentum degrades quickly out-of-sample; combining fundamentals (earnings, cash flow, debt) with options sentiment or microstructure yields stable, persistent signals.

## What Worked

- **Variance Risk Premium Arbitrage (Alpha 008):** Contrasting forward-looking implied volatility against Parkinson realized high-low volatility in large caps (`TOP200`) generates high margins (22.79 bps) with zero decay.
- **Analyst Consensus Smoothing & Winsorization (Alpha 009):** Smoothing forward net profit estimates with a 40-day window and winsorizing extreme analyst outliers (4.0 std) produces reliable forward earnings yield alpha with minimal turnover (4.51%).
- **Data Quality & NaN Handling (Alphas 010 & 011):** Enabling `NaN Handling: On` for the operating cash flow yield signal dramatically improved Sharpe from 1.84 to 2.14 and Fitness from 1.22 to 1.60 by avoiding coverage drops across the TOP3000 universe.
- **Fundamental + Derivatives Positioning Blend (Alpha 012):** Blending subindustry-ranked operating income yield with inverse options put-call open interest sentiment achieved one of the strongest portfolio performances: **2.28 Sharpe**, **1.71 Fitness**, and **28.67 bps margin** with only **5.20% turnover**.
- **Volume-decile neutralization for sentiment (Alpha 002):** Isolating social buzz across volume buckets prevents mega-cap liquidity bias.

## What Didn't Work

- Unwinsorized forward consensus metrics: extreme analyst revisions distort cross-sectional scores and trigger heavy drawdowns without winsorization.
- Running unneutralized sentiment or momentum signals: exposed to sharp market sector rotations.
- Ignoring missing data imputation on universe expansions (`TOP3000`): non-handled NaNs discard viable signals and degrade backtest fidelity.

## Platform & Data Notes

- `TOP200` universe offers cleaner options implied volatility surfaces with high liquidity and tight spreads.
- `TOP3000` provides broad dispersion for fundamental ratios, but requires robust missing value (`NaN Handling: On`) and outlier treatment.
- Combining options flow/positioning (`pcr_oi`, `implied_volatility`) with fundamental earnings consistently produces the lowest self-correlation against conventional price-volume alphas.

---

*Continuously updated as research progresses.*
