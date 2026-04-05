---
title: "zostaff — Polymarket bot guide (RBI + Claude Code)"
updated: 2026-04-05
domain: prediction-markets
tags:
  - source-summary
source_count: 1
---

# zostaff — Polymarket bot guide (RBI + Claude Code)

**Source:** X Article by [@zostaff](https://x.com/zostaff/status/2036084232519324147), saved as `raw/inbox/zostaff on X_ _How to Quit a Job You Hate. How to Build Your Own Trading Bot.A Complete Guide._ _ X.htm`.

**Note:** Mixes **pop neuroscience** (amygdala vs PFC latency — not vetted here), **hero fund anecdotes** (Simons, Citadel, etc.), and a **how-to** for [[wiki/shared/entities/polymarket|Polymarket]] bots using **Claude Code** + `py-clob-client`. Backtest win rates and PnL paths are **author illustrations**, not verified.

## Thesis (author)

- Discretionary trading loses to emotion; algorithms execute rules.
- **RBI pipeline:** **Research** (ideas from books, podcasts, Scholar, small live observation) → **Backtest** (OHLCV, metrics: win rate, profit factor, drawdown, Sharpe) → **Incubate** (tiny size, weeks of live monitoring, gradual scale).
- **Polymarket specifics:** claims **limit orders are free** vs market orders; recommends limit-only bots.
- **Example stats (author):** on “Polymarket 5-minute markets,” MACD / RSI+VWAP / CVD divergence strategies cited with ~59–63% win rates — treat as **examples**, not evidence.

## Build recipe (author)

- Use **Claude Code** to scaffold Python project: `strategies/`, `backtesting/`, `bot/`, `deploy/`, `py-clob-client`, risk manager, `.env.example`, etc.
- Parallel terminals for multiple bots/strategies; separate accounts per bot (as described).

## Critical reading

- **Survivorship and overfitting:** standard quant caveats apply; short-horizon market microstructure can change.
- **Regulatory / ToS:** automation and cross-venue latency may conflict with rules — not addressed in source.

## See also

- [[wiki/domains/llm-dev-tooling/overview]] — Claude Code as dev agent (this article is a use case).
- [[wiki/domains/prediction-markets/summary-movez-game-theory-polymarket-72m-trades]] — empirical maker/taker framing.
- [[wiki/domains/prediction-markets/overview]]
- [[wiki/domains/prediction-markets/sources-index]]
