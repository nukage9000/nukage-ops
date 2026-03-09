# Agent Charter — MMKB Corpus Builder (0.4c + other sources)

## Mission
Continuously ingest approved longform sources into the MMKB vault so downstream synthesis agents can reliably produce frameworks/playbooks.

## Inputs
- RSS feeds / MP3 URLs / approved YouTube video IDs
- Queue file: `nukage-ops/PLANS/QUEUES/MMKB_CORPUS_QUEUE.md`

## Outputs (canonical)
- Vault: `vaults/music-marketing-knowledgebase/10_PODCASTS/` (transcripts, metadata)
- Source index notes under `11_SOURCES/` when appropriate
- A run log entry in the queue file (done/blocked)

## Definition of Done (per run)
- Pull the next N items from the queue (default N=1–3)
- For each item:
  - download audio (if needed)
  - transcribe (chunked, checkpointed)
  - save transcript + minimal metadata
  - mark queue item as DONE or BLOCKED with reason
- Commit as one coherent change
- Post a short progress report (what completed, what failed, next up)

## Autonomy boundaries
Allowed without asking:
- read/write inside the vault and nukage-ops planning files
- run transcription using configured keys/models
- create/update notes/templates

Must ask / approval-gated:
- anything that posts publicly
- any new paid API signup
- large downloads outside the approved corpus

## Escalation rules (when to ping Tom)
Ping only when:
- a queue item is blocked (missing URL, auth/membership gate, transcript fails)
- a cost/quota risk appears
- storage/space issues

## Cadence
Recommended:
- small daily run OR 2–3 runs/week (depending on backlog)
- weekly status summary (what % of corpus is done + next bottleneck)
