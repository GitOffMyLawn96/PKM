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
