# WorldQuant BRAIN — Alpha Research Portfolio

![Bronze Certificate](https://img.shields.io/badge/WQ_BRAIN-Bronze_Certified-CD7F32?style=for-the-badge&labelColor=1a1a2e)
![Silver Certificate](https://img.shields.io/badge/WQ_BRAIN-Silver_Certified-C0C0C0?style=for-the-badge&labelColor=1a1a2e)
![Researcher Points](https://img.shields.io/badge/Points-7%2C864-0096FF?style=for-the-badge&labelColor=1a1a2e)
![Accepted Alphas](https://img.shields.io/badge/Accepted_Alphas-6-00C853?style=for-the-badge&labelColor=1a1a2e)

---

## About

[WorldQuant BRAIN](https://platform.worldquant.com) (Browse, Research, Alpha, Invest, Network) is a cloud-based platform for designing and testing quantitative trading signals — known as **alphas** — against historical equity data. Researchers build mathematical expressions using price, volume, fundamental, and alternative data to generate predictive signals, which are then evaluated through rigorous out-of-sample backtesting.

This repository serves as a structured record of my accepted alphas on the platform, along with research notes accumulated during the process. All alphas documented here have passed BRAIN's automated quality checks and have been formally accepted into the system.

**Researcher Level:** Silver · **Points:** 7,864

## Repository Structure

```
worldquant-brain-alphas/
├── README.md
├── accepted-alphas/
│   ├── TEMPLATE.md                          # Template for documenting new alphas
│   ├── alpha-001-market-microstructure.md
│   ├── alpha-002-scl12-sentiment.md
│   ├── alpha-003-operating-income-rank.md
│   ├── alpha-004-volatility-skew.md
│   ├── alpha-005-fcf-momentum.md
│   └── alpha-006-income-volume-blend.md
└── learning/
    └── research-notes.md
```

## Accepted Alphas

| # | Name | Universe | Neutralization | Sharpe | Fitness | Turnover | Submitted |
|---|------|----------|----------------|--------|---------|----------|-----------|
| 001 | [Market Microstructure](accepted-alphas/alpha-001-market-microstructure.md) | TOP1000 | Subindustry | 1.77 | 1.68 | 8.81% | 2026-08-06 |
| 002 | [SCL12 Sentiment](accepted-alphas/alpha-002-scl12-sentiment.md) | TOP3000 | Industry | 2.15 | 1.51 | 60.57% | 2026-08-17 |
| 003 | [Operating Income Rank](accepted-alphas/alpha-003-operating-income-rank.md) | TOP1000 | Subindustry | 1.51 | 1.28 | 8.09% | 2026-08-25 |
| 004 | [Volatility Skew](accepted-alphas/alpha-004-volatility-skew.md) | TOP3000 | Industry | 1.91 | 3.12 | 4.77% | 2026-08-25 |
| 005 | [FCF + Momentum](accepted-alphas/alpha-005-fcf-momentum.md) | TOP1000 | Industry | 1.60 | 1.21 | 7.07% | 2026-08-27 |
| 006 | [Income–Volume Blend](accepted-alphas/alpha-006-income-volume-blend.md) | TOP3000 | Subindustry | 1.91 | 4.77 | 6.91% | 2026-08-28 |

## Certificates

| Certificate | Status |
|-------------|--------|
| Bronze | ✅ Earned |
| Silver | ✅ Earned |
| Gold | ⬜ In Progress |

## Disclaimer

All alpha expressions documented here are my original research on the WorldQuant BRAIN platform. Performance metrics reflect historical out-of-sample backtests and do not guarantee future returns. This repository is intended as a personal research portfolio and educational reference.

---

*Last updated: 2026-08-28*
