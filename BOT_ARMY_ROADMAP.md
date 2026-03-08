# Nukage — Bot Army Roadmap

This repo is the home for **planning + architecture + runbooks**.

The Knowledgebase (scraped corpus + derived insights/playbooks) lives separately in:
- https://github.com/nukage9000/music-marketing-knowledgebase

## Principles
- Build small agents with clear inputs/outputs.
- Prefer approval-gated actions for anything that can spam, download media, or post publicly.
- Use budgets (max items/minutes per run, max API spend).

## Agent inventory

### 1) MMKB Corpus Builder (My .4 Cents)
- **Goal:** Ingest + transcribe My .4 Cents into a searchable corpus.
- **Sources:**
  - Acast RSS MP3 feed (primary)
  - YouTube captions (bonus)
- **Transcription:** Groq Whisper (`whisper-large-v3-turbo`)
- **Status:** Active / in progress
- **Outputs (KB repo):** `10_PODCASTS/0.4c/Acast/Transcripts/*`

### 2) Framework Synthesizer
- **Goal:** Convert corpus into frameworks + SOP playbooks.
- **Priority domains:** Meta ads, short-form content, release strategy.
- **Status:** Planned

### 3) DJ Taste Profiler (Listening → Taste Map)
- **Goal:** Given your YouTube playlist of mixes, infer taste clusters + adjacent scenes + audience hypotheses.
- **Status:** Planned

### 4) Trend Watcher (Taste-aligned)
- **Goal:** Track fast-moving trends filtered through your taste profile.
- **Status:** Planned

### 5) Playlist/Crate Builder
- **Goal:** Build weekly/monthly crates from trend signals + taste.
- **Status:** Planned (approval-gated)

### 6) Downloader / Library Manager
- **Goal:** Download approved tracks/mixes for offline review / DJ prep.
- **Status:** Planned (approval-gated)

### 7) Local Scene Analyzer
- **Goal:** Map your local scene (venues, events, DJs, artists) and surface high-bar opportunities.
- **Status:** Planned
- **Needs:** city/region, travel radius, genre/vibe constraints, opportunity definition.
