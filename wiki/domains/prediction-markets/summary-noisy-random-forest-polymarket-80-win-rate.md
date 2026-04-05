---
title: "Noisy — Random Forest + Polymarket (80% win-rate claim)"
updated: 2026-04-05
domain: prediction-markets
tags:
  - source-summary
source_count: 1
---

# Noisy — Random Forest + Polymarket (80% win-rate claim)

**Source:** X Article by [@noisyb0y1](https://x.com/noisyb0y1/status/2033856891181220265), saved as `raw/inbox/Noisy on X_ _100+ signals , 38 indicators. How we hit 80_ win rate with Ai and math_ _ X.htm`.

**Note:** **Separate** from [[wiki/domains/llm-dev-tooling/summary-noisy-claude-code-plugins-five|Noisy’s Claude Code plugins piece]]. Heavy **Telegram CTA**; performance numbers **unverified**.

## Method (as described)

- **Ensemble:** **Random Forest** treated as “100+ models” voting; feature count per tree \(\approx \sqrt{\text{total features}}\).
- **Output:** probability of YES in \([0,1]\); enter when **≥ 70%** “confidence.”
- **Entry filter:** buy only when market price \(\leq 0.5 \times p_{\text{model}}\) (example: market 28% vs model 65%).
- **Evaluation:** prefers **Sharpe ratio** over raw win rate; mentions **log returns** for path-dependent PnL; **MAE** / **MFE** for exit diagnostics.
- **Income claim:** “\$20,000+ a week” — **anecdotal**.

## See also

- [[wiki/domains/llm-dev-tooling/summary-noisy-claude-code-plugins-five]] — same author, different topic.
- [[wiki/domains/prediction-markets/summary-lunar-polymarket-math-blueprint]] — EV / Kelly framing on Polymarket.
- [[wiki/domains/prediction-markets/overview]]
- [[wiki/domains/prediction-markets/sources-index]]
