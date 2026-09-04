# WorldQuant BRAIN — Alpha Research Portfolio

![Bronze Certificate](https://img.shields.io/badge/WQ_BRAIN-Bronze_Certified-CD7F32?style=for-the-badge&labelColor=1a1a2e)
![Silver Certificate](https://img.shields.io/badge/WQ_BRAIN-Silver_Certified-C0C0C0?style=for-the-badge&labelColor=1a1a2e)
![Gold Certificate](https://img.shields.io/badge/WQ_BRAIN-Gold_Certified-FFD700?style=for-the-badge&labelColor=1a1a2e)
![Researcher Points](https://img.shields.io/badge/Points-20%2C000%2B-0096FF?style=for-the-badge&labelColor=1a1a2e)
![Accepted Alphas](https://img.shields.io/badge/Accepted_Alphas-14-00C853?style=for-the-badge&labelColor=1a1a2e)
![License](https://img.shields.io/badge/License-All_Rights_Reserved-FF5722?style=for-the-badge&labelColor=1a1a2e)

---

## About

[WorldQuant BRAIN](https://platform.worldquant.com) (Browse, Research, Alpha, Invest, Network) is a quantitative simulation platform for developing and deploying predictive equity trading signals (**alphas**) across global markets. Researchers construct mathematical hypotheses leveraging market, fundamental, and alternative datasets, rigorously evaluated via out-of-sample (OS) performance metrics and correlation penalties.

This repository documents my accepted quantitative signals on the platform, detailing core architectural intuition, factor structures, neutralization schemes, and out-of-sample performance characteristics.

> 🔒 **Code Protection Note:** To safeguard proprietary alpha expressions and prevent front-running/duplication, exact formulas are omitted. High-level architecture, factor mechanics, and backtest results are documented. **Full formulas are available upon request — DM on LinkedIn.**

**Researcher Level:** Gold · **Points:** 20,000+

---

## Repository Structure

```
worldquant-brain-alphas/
├── README.md
├── LICENSE
├── accepted-alphas/
│   ├── TEMPLATE.md                              # Template for documenting new alphas
│   ├── alpha-001-market-microstructure.md
│   ├── alpha-002-scl12-sentiment.md
│   ├── alpha-003-operating-income-rank.md
│   ├── alpha-004-volatility-skew.md
│   ├── alpha-005-fcf-momentum.md
│   ├── alpha-006-income-volume-blend.md
│   ├── alpha-007-mean-reversion-leverage.md
│   ├── alpha-008-implied-parkinson-vol-ratio.md
│   ├── alpha-009-consensus-earnings-yield.md
│   ├── alpha-010-operating-cashflow-rank.md
│   ├── alpha-011-robust-cashflow-quality.md
│   ├── alpha-012-income-options-sentiment-blend.md
│   ├── alpha-013-volume-surge-reversion.md
│   └── alpha-014-value-quality-blend.md
└── learning/
    └── research-notes.md
```

---

## Accepted Alphas

| # | Strategy / Name | Universe | Neutralization | Sharpe | Fitness | Turnover | Focus |
|---|-----------------|----------|----------------|--------|---------|----------|-------|
| 001 | [Market Microstructure](accepted-alphas/alpha-001-market-microstructure.md) | TOP1000 | Subindustry | 1.77 | 1.68 | 8.81% | Microstructure & Conditional Momentum |
| 002 | [SCL12 Sentiment](accepted-alphas/alpha-002-scl12-sentiment.md) | TOP3000 | Industry | 2.15 | 1.51 | 60.57% | Sentiment & Volume Interaction |
| 003 | [Operating Income Rank](accepted-alphas/alpha-003-operating-income-rank.md) | TOP1000 | Subindustry | 1.51 | 1.28 | 8.09% | Fundamental Quality & Profitability |
| 004 | [Volatility Skew](accepted-alphas/alpha-004-volatility-skew.md) | TOP3000 | None | 1.91 | 3.12 | 4.77% | Options Implied Volatility Surface |
| 005 | [FCF + Momentum](accepted-alphas/alpha-005-fcf-momentum.md) | TOP1000 | Industry | 1.60 | 1.21 | 7.07% | Multi-Factor Value & Momentum |
| 006 | [Income–Volume Blend](accepted-alphas/alpha-006-income-volume-blend.md) | TOP3000 | Subindustry | 1.91 | 4.77 | 6.91% | Multi-Factor Profitability & Volume |
| 007 | [Mean Reversion + Leverage](accepted-alphas/alpha-007-mean-reversion-leverage.md) | TOP3000 | Industry | 1.40 | 1.32 | 21.77% | Price Reversion & Balance Sheet Leverage |
| 008 | [Implied vs Parkinson Vol](accepted-alphas/alpha-008-implied-parkinson-vol-ratio.md) | TOP200 | Sector | 1.39 | 1.48 | 21.52% | Volatility Surface Arbitrage & Variance Risk |
| 009 | [Consensus Earnings Yield](accepted-alphas/alpha-009-consensus-earnings-yield.md) | TOP3000 | None | 1.46 | 1.43 | 4.51% | Analyst Consensus Profitability & Forward PE |
| 010 | [Operating Cash Flow Rank](accepted-alphas/alpha-010-operating-cashflow-rank.md) | TOP3000 | Subindustry | 1.84 | 1.22 | 18.50% | Cash Flow Yield & Capital Efficiency |
| 011 | [Robust Cash Flow Quality](accepted-alphas/alpha-011-robust-cashflow-quality.md) | TOP3000 | Subindustry | 2.14 | 1.60 | 17.07% | Cash Generation with Missing Data Imputation |
| 012 | [Income & Options Sentiment](accepted-alphas/alpha-012-income-options-sentiment-blend.md) | TOP3000 | Subindustry | 2.28 | 1.71 | 5.20% | Profitability Return & Put-Call Sentiment Blend |
| 013 | [Volume-Surge Reversion](accepted-alphas/alpha-013-volume-surge-reversion.md) | TOP3000 | Subindustry | 2.03 | 1.07 | 48.70% | Short-Term Price Reversion & Volume Surge |
| 014 | [Value & Quality Blend](accepted-alphas/alpha-014-value-quality-blend.md) | TOP3000 | Subindustry | **2.65** | **2.05** | 19.79% | Book-to-Market & ROE Capital Efficiency |

---

## Certificates

| Certificate | Status |
|-------------|--------|
| Bronze | ✅ Earned |
| Silver | ✅ Earned |
| Gold | ✅ Earned |

---

## License & Intellectual Property

This project is licensed under a proprietary **All Rights Reserved** license — see the [LICENSE](LICENSE) file for details. Signals and research are displayed strictly for portfolio and educational demonstration.

---

*Last updated: 2026-09-04*
