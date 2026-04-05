# PKM wiki — agent schema

This repository follows the pattern in [README.md](README.md): a **three-layer** personal knowledge system maintained by an LLM agent, browsed in **Obsidian**. You (the agent) own the **wiki** layer; you never modify **raw** sources.

## Layers

| Layer | Path | Rule |
|--------|------|------|
| **Raw sources** | `raw/` | **Read only.** Never create, edit, move, or delete files here. Source of truth for articles, papers, clips, images. Use `raw/inbox/` as a drop zone if the human adds files before filing. Attachments / downloaded images: `raw/assets/` (Obsidian: set default attachment folder to this path). |
| **Wiki** | `wiki/` | **You maintain this.** Markdown only unless the human asks otherwise. Create and update pages, wikilinks, summaries, entity/concept pages, and cross-references. |
| **Schema** | `AGENTS.md` (this file), optionally `CLAUDE.md` | Conventions and workflows. Co-evolve with the human when something stops working. |

**Obsidian:** Open the **repository root** as the vault so paths like `wiki/...` resolve. Use wikilinks with paths from vault root, e.g. `[[wiki/overview]]`, `[[wiki/domains/my-topic/overview]]`.

## Operations

### Ingest

When the human adds a source under `raw/` and asks you to process it:

1. Read the source (and any linked images under `raw/assets/` if relevant).
2. Discuss key takeaways with the human if useful.
3. Write or update wiki pages: summary, entities, concepts, domain overviews as appropriate.
4. Update [[wiki/index]]: add/update rows in the right sections (domains, shared, source summaries, filed answers).
5. Append [[wiki/log]] with `## [YYYY-MM-DD] ingest | <short title>` and a brief note of what changed.

A single source may touch many pages (often 10–15); that is expected.

### Query

When the human asks questions against the wiki:

1. Read [[wiki/index]] first to find relevant pages, then open those files.
2. Synthesize an answer with citations (wikilinks or paths to wiki pages).
3. If the answer is durable (comparison, analysis, important connection), **file it** as a new wiki page and add it to [[wiki/index]] under **Filed answers** (or the best section). Append [[wiki/log]] with `## [YYYY-MM-DD] query | <short title>` when you file something substantial.

### Lint

When the human asks for a wiki health check (or periodically):

1. Look for **contradictions** between pages.
2. **Stale claims** superseded by newer sources or newer wiki text.
3. **Orphan pages** with no inbound wikilinks (excluding intentional stubs).
4. **Missing pages** for important concepts or entities that are mentioned repeatedly.
5. **Missing cross-references** where links would help navigation.
6. **Gaps** that could be filled with new sources or a web search.

Summarize findings for the human; apply fixes they approve. Append [[wiki/log]] with `## [YYYY-MM-DD] lint | <short title>`.

## Index and log

- **[[wiki/index]]** — Content catalog. Update on every ingest (and when filing major query outputs). Keep one-line summaries accurate. Organize by: Overview, Domains, Shared concepts, Shared entities, Source summaries, Filed answers (adjust as needed).
- **[[wiki/log]]** — Append only. Use consistent heading prefixes: `## [YYYY-MM-DD] ingest | ...`, `query | ...`, `lint | ...` so entries are easy to grep.

## Topic branches (domains)

Unrelated subjects live in **parallel** under `wiki/domains/<slug>/` (kebab-case, e.g. `crypto-hft`, `space-systems`).

**New domain procedure:**

1. Create `wiki/domains/<slug>/`.
2. Copy from `wiki/domains/_template/` into the new folder (at minimum `overview.md` and `sources-index.md`).
3. Fill `overview.md` with scope, open questions, and links to [[wiki/overview]] and any `wiki/shared/` pages.
4. Add the domain to [[wiki/index#Domains]] and a short link line in [[wiki/overview]].
5. Log: `## [YYYY-MM-DD] ingest | domain: <slug>` or a dedicated `setup` line if you prefer.

Optional: add `MOC-<topic>.md` (map of content) when a domain grows large.

## Naming and linking

- **Folders:** `kebab-case`.
- **Wikilinks:** Obsidian-style, path from vault root, no extension: `[[wiki/domains/foo/overview]]`, optional display text: `[[wiki/domains/foo/overview|Foo]]`.
- Prefer linking to the **canonical** page for a concept or entity (usually under `wiki/shared/` if cross-domain, else under the domain).

## Frontmatter (optional, Dataview-friendly)

On wiki pages when useful, use YAML frontmatter:

```yaml
---
title: Page title
updated: YYYY-MM-DD
domain: crypto-hft   # or shared, meta, etc.
tags: [concept]
source_count: 0      # approximate, when summarizing raw sources
---
```

## Scale and tooling

- At moderate scale, [[wiki/index]] is the primary navigation aid for you and the human.
- When the wiki grows very large, consider **local search** (e.g. [qmd](https://github.com/tobi/qmd)) — hybrid search + optional MCP — or a small custom search script. Document chosen tooling in this file when adopted.
- Optional **markdownlint** (see repo `package.json`) helps mechanical consistency; do not let it block useful LLM prose — fix trivial violations when the human runs lint.

## Summary

**Raw = read-only. Wiki = you maintain. Always update index + log on ingest; file good query answers; lint on request.**
