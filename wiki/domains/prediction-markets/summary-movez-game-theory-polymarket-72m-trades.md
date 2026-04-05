---
title: "Movez — Game theory on Polymarket (five formulas, 72M trades)"
updated: 2026-04-05
domain: prediction-markets
tags:
  - source-summary
source_count: 1
---

# Movez — Game theory on Polymarket (five formulas, 72M trades)

**Source:** Saved X Article by [@0xMovez](https://x.com/0xMovez/status/2037499562064073209) — *“Game Theory on Polymarket: The 5 Formulas tested on 72 million trades”* (HTML under `raw/inbox/`).

**Note:** Statistics, PnL examples, and equilibrium claims below are **from the article** (often attributed to researcher **Jonathan Becker** on **Kalshi** data); the author argues the same biases apply to [[wiki/shared/entities/polymarket|Polymarket]]. None of this has been independently checked in this vault.

## Framing (author)

- **Scale cited:** 72.1M trades and \$18.26B volume across resolved Kalshi markets (per Becker), paralleled to Polymarket mechanics and trader psychology.
- **Headline split:** ~87% of wallets lose; top ~13% use explicit math (EV, tail mispricing, Kelly, Bayes, Nash-style maker/taker balance).
- **Illustrative traders:** e.g. “RN” (+\$6M sports PnL) and “distinct-baguette” (\$560 → \$812K market-making) — **anecdotal**, linked to Polymarket profiles in the original piece.

## The five formula areas

### 1) Expected value (EV)

- Bets framed as repeated EV problems; example: YES at 12¢ vs model \(p = 20\%\) → positive EV vs implied 12%.
- **Empirical claim (article):** average **taker** (market order) **−1.12%** per trade vs **maker** (limit) **+1.12%** over the large sample — attributed to patience / waiting for +EV vs impulse.

### 2) Mispricing at the tails (“cheap contract trap”)

- **Longshot bias (author):** low-price contracts win **less often** than their prices imply; example band: 5¢ contracts win ~**4.18%** → **−16.36%** “mispricing” vs 5% fair; 1¢ taker wins ~**0.43%** → **−57%** mispricing (Kalshi calibration narrative).
- **Calibration story:** efficient ~30–70¢; inefficiency concentrated below ~20¢ and above ~80¢.
- **Two metrics in the piece:** (a) mispricing \(\delta\) — deviation of realized win rate from implied probability; (b) **gross excess return** \(r_i\) per outcome — highlights huge upside on rare wins vs −100% loss, lottery-style psychology.
- **Return-on-\$1 table (author):** e.g. ~\$0.43 back per \$1 in 1¢ taker buckets vs ~\$1.02 on 90¢ contracts — **monotonic** “cheaper = worse for takers”; makers described as near mirror image.
- **Takeaway stated:** sell/overweight longshots, buy near-certainties (directional framing, not personalized advice).

### 3) Kelly criterion (sizing)

- Binary contract odds \(b\) as profit/risk ratio (e.g. 30¢ YES → \(b = 0.70/0.30\)).
- **Fractional Kelly:** full Kelly as long-run growth-optimal but **high drawdown**; article pushes quarter/half Kelly and lookup-style tables / calculators.

### 4) Bayesian updating

- \(P(H\mid E)\) with law of total probability; Fed rate-cut example with likelihoods for weak jobs report under “cut” vs “no cut.”
- **Likelihood ratio** shortcut and “evidence moves you most when uncertain” (mid priors).

### 5) Nash equilibrium (maker–taker / “poker bluff” analogy)

- **Mapping (author):** bluff frequency ↔ contrarian liquidity provision; value bet ↔ conviction with crowd; pot odds ↔ break-even thresholds.
- **Indifference / equilibrium:** marginal trader indifferent between maker and taker at equilibrium (conceptual).
- **Time-varying meta (author):** before **Oct 2024** optimal mix ~**60%+ taker** (amateur makers lose); after volume spike and pros, flips to ~**65–70% maker**; taker “edge” said to have compressed (e.g. +2% in 2022 → −1.12% in the cited aggregate).

## Critical reading

- **Venue transfer:** Kalshi-derived calibration and percentages may **not** map 1:1 to Polymarket (fees, participant mix, resolution rules, time period).
- **Selection and survivorship:** wallet-level loss rates and hero PnL stories need careful interpretation.
- **Equilibrium shift narrative** is a strong causal story from one article; treat as hypothesis.

## See also

- [[wiki/domains/prediction-markets/summary-bl888m-polymarket-wallet-narrative]] — first-person wallet-copy narrative (same rough 87/13 meme; advertorial; unverified PnL).
- [[wiki/domains/prediction-markets/summary-aleiah-polymarket-quant-playbook-2026]] — complementary “six formulas” playbook (LMSR, KL, Bregman, etc.).
- [[wiki/domains/prediction-markets/overview]]
- [[wiki/domains/prediction-markets/sources-index]]
