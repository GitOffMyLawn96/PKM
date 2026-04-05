---
title: "karpathy — autoresearch (agents + single-GPU nanochat)"
updated: 2026-04-05
domain: llm-dev-tooling
tags:
  - source-summary
source_count: 1
---

# karpathy — autoresearch (agents + single-GPU nanochat)

**Source:** Saved GitHub repo page HTML for [karpathy/autoresearch](https://github.com/karpathy/autoresearch) (`raw/inbox/karpathy_autoresearch_ AI agents running research on single-GPU nanochat training automatically.htm`).

## Stated focus (from repo title / description)

- **Autonomous research agents** applied to **nanochat**-style model **training** on a **single GPU** — i.e. closing the loop between experimentation and training without large clusters (exact methodology: see upstream `README.md`, `program.md`, and `train.py`).

## Repo surface (from embedded file tree in the save)

- Notable files: `train.py`, `prepare.py`, `program.md`, `analysis.ipynb`, `pyproject.toml`, `uv.lock` — suggests a small Python project with locked dependencies and an explicit “program” spec for the agent loop.

## Notes

- This vault does **not** reproduce training results; link to the repository for install, safety, and compute requirements.

## See also

- [[wiki/domains/llm-dev-tooling/summary-kevin-gu-autoagent]] — another OSS “meta-agent / harness” angle.
- [[wiki/domains/llm-dev-tooling/overview]]
- [[wiki/domains/llm-dev-tooling/sources-index]]
