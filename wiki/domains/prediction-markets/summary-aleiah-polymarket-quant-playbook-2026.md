---
title: "Aleiah — Polymarket quant playbook (six formulas)"
updated: 2026-04-05
domain: prediction-markets
tags:
  - source-summary
source_count: 1
---

# Aleiah — Polymarket quant playbook (six formulas)

**Source:** Saved X Article by [@AleiahLock](https://x.com/AleiahLock/status/2040799934752981079) — *“The Quant Playbook for Polymarket: 6 Formulas Hedge Funds Use to Extract Millions in 2026”* (HTML save under `raw/inbox/`).

**Note:** Dollar figures, hit rates, and “edge” examples below are **claims in the article**, not independently verified.

## Thesis (author)

- Prediction markets (especially [[wiki/shared/entities/polymarket|Polymarket]]) are framed as increasingly “quant competitive,” not only retail gambling.
- A structured stack (pricing model → sizing → mispricing scans → correlated markets → multi-outcome optimization → belief updating) is presented as copyable in part by retail traders with APIs and Python.

## Six formulas (outline)

1. **LMSR / liquidity parameter** — Treat Logarithmic Market Scoring Rule style pricing as core; author gives \( \text{Price}_i = e^{q_i/b} / \sum_j e^{q_j/b} \) with \(q\) as outcome quantities and \(b\) as liquidity depth. Emphasis on **price impact** in thin pools (small \(b\)); example: BTC short-horizon market, ~5% move from a small YES buy. **Risks:** manipulation when \(b<50\); check volume. Suggested homework: plot impact vs size using API \(b\).

2. **Kelly criterion** — Fractional Kelly for growth vs ruin; \(f^* = (p \cdot \text{odds} - (1-p))/\text{odds}\) with odds tied to price; author recommends fractional (0.25–0.5×). Example: political market with model \(p\) above market. **Risk:** overestimating \(p\). Homework: backtest on historical resolutions.

3. **EV gap** — \( \mathrm{EV} = (p_{\text{true}} - \text{price}) \times \text{payout} \) with payout \(\approx 1/\text{price}\); author suggests acting only if EV clears a threshold after fees (e.g. > 0.05). Example: geopolitical market vs news-based model. Homework: pull chain/API data and compare to model \(p\).

4. **KL divergence** — \(D_{KL}(P\|Q) = \sum_i P_i \log(P_i/Q_i)\) between correlated market probability vectors; author uses a threshold (e.g. > 0.2) as a mispricing / relative-consistency flag. Example: correlated 2028 political markets. **Risk:** noise in low volume.

5. **Bregman projection** — Minimize a Bregman divergence (often KL) subject to probability polytope constraints to find **multi-outcome** “arb-feasible” marginals; author notes compute cost and iterative solvers. Example: Oscar-style multi-candidate markets.

6. **Bayes’ rule** — \(P(H|E) = P(E|H)P(H)/P(E)\) for updating hypotheses on streaming evidence (social, polls). Example: fast-moving narrative market.

## “Build a bot” checklist (author)

- Polygon / venue APIs for odds and liquidity.
- Python stack: numpy, scipy, cvxpy (as needed).
- Walk-forward backtests; deploy via cron (e.g. Railway/GitHub); alerts (e.g. Telegram).
- Risk: fractional Kelly, drawdown stop; watch overfitting and fee drag.

## Critical reading

- Venue mechanics and fee schedules change; treat the article’s “LMSR / \(b\) parameter” story as a **modeling lens** unless confirmed against current Polymarket docs and APIs.
- Performance numbers are illustrative or anecdotal in the piece; treat as motivation, not evidence.
- **Ethics:** author flags sensitivity of betting on real-world harm (e.g. conflict).

## See also

- [[wiki/domains/prediction-markets/summary-bl888m-polymarket-wallet-narrative]] — wallet-scan / copy-trade story (promotional; unverified).
- [[wiki/domains/prediction-markets/summary-movez-game-theory-polymarket-72m-trades]] — empirical / game-theory framing (Kalshi-scale stats, maker–taker, tail mispricing).
- [[wiki/shared/entities/polymarket]]
- [[wiki/domains/prediction-markets/overview]]
- [[wiki/domains/prediction-markets/sources-index]]
