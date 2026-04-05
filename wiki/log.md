# Wiki log

Append-only timeline of **ingests**, **queries** (when something material was filed), and **lint** passes. Use a consistent heading prefix so entries stay easy to grep.

Suggested prefix pattern:

`## [YYYY-MM-DD] ingest | Short title`

`## [YYYY-MM-DD] query | Short title`

`## [YYYY-MM-DD] lint | Short title`

Example (PowerShell): recent headings only — adapt as needed.

---

## [2026-04-05] setup | Initial PKM layout

Vault structure created: `raw/` (sources), `wiki/` (LLM-maintained), schema at repo root (`AGENTS.md`). Domains `crypto-hft` and `space-systems` stubbed with overview pages.

## [2026-04-05] ingest | Aleiah X article — Polymarket quant playbook

Ingested saved X Article (HTML + `_files`) from `raw/inbox/`: *The Quant Playbook for Polymarket* ([@AleiahLock](https://x.com/AleiahLock/status/2040799934752981079)). Added domain [[wiki/domains/prediction-markets/overview|prediction-markets]], source summary [[wiki/domains/prediction-markets/summary-aleiah-polymarket-quant-playbook-2026]], entity [[wiki/shared/entities/polymarket]], updated [[wiki/index]] and [[wiki/overview]].

## [2026-04-05] ingest | Movez X article — game theory on Polymarket

Ingested saved X Article from `raw/inbox/`: *Game Theory on Polymarket: The 5 Formulas tested on 72 million trades* ([@0xMovez](https://x.com/0xMovez/status/2037499562064073209)). New summary [[wiki/domains/prediction-markets/summary-movez-game-theory-polymarket-72m-trades]]; updated [[wiki/domains/prediction-markets/sources-index]], cross-link on [[wiki/domains/prediction-markets/summary-aleiah-polymarket-quant-playbook-2026]], [[wiki/index]].

## [2026-04-05] ingest | bl888m X article — Polymarket wallet narrative

Ingested saved X Article from `raw/inbox/`: *How I Made $51K on Polymarket Without Knowing How to Trade* ([@bl888m](https://x.com/bl888m/status/2040097622459838967)). New summary [[wiki/domains/prediction-markets/summary-bl888m-polymarket-wallet-narrative]] (advertorial / unverified PnL caveats); updated [[wiki/domains/prediction-markets/sources-index]], cross-links from [[wiki/domains/prediction-markets/summary-movez-game-theory-polymarket-72m-trades]] and [[wiki/domains/prediction-markets/summary-aleiah-polymarket-quant-playbook-2026]], [[wiki/index]].

## [2026-04-05] ingest | inbox batch — five new X articles (no re-index of prior sources)

**Skipped (already in [[wiki/domains/prediction-markets/sources-index]]):** Movez 72M trades, bl888m 51K narrative, Aleiah Polymarket quant playbook (those `.htm` names unchanged).

**New domains:** [[wiki/domains/llm-dev-tooling/overview|llm-dev-tooling]], [[wiki/domains/llm-monetization/overview|llm-monetization]], [[wiki/domains/org-ai-futures/overview|org-ai-futures]].

**New summaries:** [[wiki/domains/llm-dev-tooling/summary-kevin-gu-autoagent]] (Kevin Gu / AutoAgent), [[wiki/domains/llm-dev-tooling/summary-noisy-claude-code-plugins-five]] (Noisy plugins), [[wiki/domains/org-ai-futures/summary-jack-hierarchy-to-intelligence-block]] (jack / Block hierarchy essay), [[wiki/domains/prediction-markets/summary-zostaff-polymarket-bot-rbi-claude-code]] (zostaff RBI bot guide), [[wiki/domains/llm-monetization/summary-aleiah-seventeen-claude-skills-monetization]] (Aleiah 17 skills — distinct from Polymarket playbook). Updated [[wiki/index]], [[wiki/overview]], domain `sources-index` files.

## [2026-04-05] ingest | Hanako X article — six Claude Polymarket strategies

New inbox save: `(1) Hanako on X_ ...Prediction Markets Overlook...htm`. Summary [[wiki/domains/prediction-markets/summary-hanako-claude-six-polymarket-strategies]]; updated [[wiki/domains/prediction-markets/sources-index]], [[wiki/index]] (inbox note: goose + Hanako present).

## [2026-04-05] ingest | block/goose GitHub save + inbox cleared

Human removed prior `raw/inbox/` HTML; only `block_goose_...htm` remains. New summary [[wiki/domains/llm-dev-tooling/summary-block-goose]]. Updated all domain `sources-index` tables and [[wiki/index]] source table to mark **removed from inbox** vs **present** snapshot.

## [2026-04-05] ingest | inbox batch — seven new sources only (deduped)

Compared `raw/inbox/*.htm` to existing `sources-index` / [[wiki/index]] rows; **did not** add second rows for already-indexed: Movez, bl888m, zostaff, Kevin Gu, Noisy plugins, jack, Aleiah 17 skills.

**New domain:** [[wiki/domains/media-automation/overview|media-automation]].

**New summaries:** [[wiki/domains/media-automation/summary-fujiwarachoki-moneyprinter]], [[wiki/domains/llm-dev-tooling/summary-karpathy-autoresearch]], [[wiki/domains/org-ai-futures/summary-mirofish-god-view-engine]], [[wiki/domains/prediction-markets/summary-lunar-polymarket-math-blueprint]], [[wiki/domains/prediction-markets/summary-noisy-random-forest-polymarket-80-win-rate]], [[wiki/domains/llm-monetization/summary-ernesto-openclaw-eddie-ads]], [[wiki/domains/llm-monetization/summary-zephyr-skills-500-hour-2027]]. Fixed broken wikilink in [[wiki/domains/org-ai-futures/sources-index]] (jack page slug). Cross-link: Noisy plugins → Noisy RF summary.
