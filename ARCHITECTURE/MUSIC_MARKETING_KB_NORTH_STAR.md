# Music Marketing Knowledgebase — North Star (Canonical)

This is the *shared mission* for all music-marketing agents.

## Mission
Build a **compounding music marketing operating system** for Nukage:
- a vault of **reusable frameworks and executable playbooks** (not just notes)
- grounded in **real sources** (podcasts/videos/articles) with **tight citations**
- that improves every week, and survives tool churn.

## Primary KPI (the one that matters)
**# of high-quality, re-usable playbooks shipped per month** (with citations + checklists) that Tom can actually run.

Secondary KPIs:
- Frameworks shipped/week
- % of frameworks with timestamped citations
- “Time to action”: how fast a new source becomes a usable playbook

## What “good output” looks like
- Short, actionable docs.
- Clear decision rules.
- Checklists and defaults.
- Failure modes + what to do when it breaks.
- Metrics to track.
- Links back to sources (URL + timestamp range if video).

## Guardrails (non-negotiables)
- **No transcript dumping.** Prefer derived notes + short quotes only.
- **Citations are required** for claims framed as “Jesse says…” or “the guest claims…”
- **Small, reviewable commits.** One coherent commit per ingestion run.
- **Approval-gated for anything external** (posting, emailing, downloading copyrighted media).

## Standard pipeline (one source → artifacts)
For each source, produce:
1) Entity note (if new)
2) Source note (tight summary + key timestamps)
3) 3–7 Framework notes
4) 1–3 Playbook notes
5) Commit + short progress report

## Where the work lives (canonical)
- Knowledgebase vault: `vaults/music-marketing-knowledgebase/`
- Planning + runbooks: `nukage-ops/`

## Reporting expectations (keep Tom in the loop without noise)
Every run should end with a short message:
- What was processed
- Files created/updated
- What’s next
- Blockers (with a concrete “here’s what I need from you”)

## Current known blockers (as of now)
- Members-only sources (YouTube Join) block captions/transcripts → citations missing until unlocked.
- Browser automation/service availability affects transcript extraction.
- Search discovery uses SearXNG (local) rather than paid Brave.
