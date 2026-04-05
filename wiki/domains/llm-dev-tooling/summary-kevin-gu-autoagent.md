---
title: "Kevin Gu — AutoAgent (OSS)"
updated: 2026-04-05
domain: llm-dev-tooling
tags:
  - source-summary
source_count: 1
---

# Kevin Gu — AutoAgent (OSS)

**Source:** X Article / thread by [@kevingu](https://x.com/kevingu/status/2039843234760073341), saved as `raw/inbox/Kevin Gu on X_ _AutoAgent_ first open source library for self-optimizing agents_ _ X.htm`.

## What it is (author)

- **AutoAgent:** open-source library where a **meta-agent** iteratively improves a **task agent’s harness** (prompts, tools, orchestration) against a domain benchmark.
- **Repo:** [github.com/kevinrgu/autoagent](https://github.com/kevinrgu/autoagent)
- **Claimed results (author):** after 24+ hours of autonomous iteration, #1 on **SpreadsheetBench** (96.5%) and **TerminalBench** (55.1% GPT-5 score) — stated as beating hand-tuned leaderboard entries.

## Mechanism

- Minimal starter: task agent begins with **bash tool** only; `program.md` steers research; `agent.py` is the task agent; **Harbor** adapter connects to benchmarks.
- Loop: edit harness → run tasks → measure → read **failure traces** → keep wins, revert failures → repeat, with thousands of parallel sandboxes (as described).

## Ideas named in the piece

- **“Model empathy”** — meta-agent shares weights / reasoning style with task agent when both are the same model; author reports same-model meta+task beats cross-model pairings.
- **Traces over scores only** — without trajectories, improvement allegedly stalls.
- **Overfitting to rubric** — mitigated via self-reflection prompt: would this harness change still help if the exact eval task vanished?
- **Meta-agent quality** — author claims Codex as meta-agent underperformed (stops improving early).

## Critical reading

- Leaderboard claims need independent verification and may depend on benchmark version and submission rules.
- Piece teases a future commercial product (“early access in comments”).

## See also

- [[wiki/domains/llm-dev-tooling/summary-noisy-claude-code-plugins-five]] — Claude Code ecosystem plugins.
- [[wiki/domains/llm-dev-tooling/overview]]
- [[wiki/domains/llm-dev-tooling/sources-index]]
