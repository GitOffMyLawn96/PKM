---
title: "Hanako — six Claude backtested Polymarket strategies"
updated: 2026-04-05
domain: prediction-markets
tags:
  - source-summary
source_count: 1
---

# Hanako — six Claude backtested Polymarket strategies

**Source:** X Article by [@hanakoxbt](https://x.com/hanakoxbt/status/2038645282317971848), saved as `raw/inbox/(1) Hanako on X_ _How Claude Extracts Consistent Edge From What Prediction Markets Overlook_ _ X.htm`.

**Note:** Claims **3,000+ backtests**, **800** [[wiki/shared/entities/polymarket|Polymarket]] markets, **14 months** of data, and live performance are **author-side** and **not verified** here. Piece includes a **Telegram** CTA.

## Premise (author)

- Feed **Claude** a strategy + historical resolved markets; most ideas **fail** quickly or overfit to one category; **six** patterns allegedly survive across categories, volatility, and liquidity.
- Shared theme: **no oracle** — exploit **repeated structural mistakes** (psychology + microstructure), not event prediction.

## Six strategies (outline)

1. **Base rate audit** — Compare headline/narrative prices to **historical frequencies** for analogous events (e.g. bills reaching votes); trade divergence (example: market 45% vs estimated 18% base rate → lean **sell** YES).
2. **Conditional probability / joint mispricing** — Cross-check **related** contracts (e.g. state vs national vs joint outcomes); flag violations of \(P(A \cap B) \leq \min(P(A),P(B))\) and implied \(P(A\mid B)\) vs empirical bases.
3. **Liquidity vacuum / microstructure** — Scan thin books; treat large **non-news** prints as **slippage** and bet **short-term reversion** (author: monitor hundreds of markets on a cadence; limits on empty books).
4. **Cross-venue “delta” structures** — **Polymarket vs Kalshi / others** on correlated but non-identical events; outcome matrices and weighted EV across scenarios rather than pure two-leg arb (fees/liquidity).
5. **Calibration / favorite–longshot** — Bucket resolved history by price deciles; if e.g. **85–95¢** resolves YES **less** often than price implies, systematically **fade** highs and **buy** lows (Kelly sizing claimed).
6. **Time decay** — Long-dated markets where **little happens** toward deadline; model **implied daily decay** vs base rate of action; **short** overpriced YES when time works against the event (bond MM analogy).

## Critical reading

- **Backtest narrative ≠ OOS proof:** survivor bias in “six that survived” is easy even with many tests.
- **Operational risk:** latency, fees, resolution rules, and ToS differ by venue; cross-venue structures need legal/compliance context outside this note.
- Overlaps with [[wiki/domains/prediction-markets/summary-lunar-polymarket-math-blueprint]] (base rates, calibration) and [[wiki/domains/prediction-markets/summary-movez-game-theory-polymarket-72m-trades]] (tail mispricing) — compare claims, don’t merge blindly.

## See also

- [[wiki/domains/prediction-markets/summary-lunar-polymarket-math-blueprint]]
- [[wiki/domains/prediction-markets/summary-movez-game-theory-polymarket-72m-trades]]
- [[wiki/domains/prediction-markets/overview]]
- [[wiki/domains/prediction-markets/sources-index]]
