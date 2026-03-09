# Agent Blockers & Prereqs

This file tracks what each planned agent needs before it can run smoothly and safely.

Legend:
- ✅ ready
- 🟡 partial / can start with manual inputs
- 🔴 blocked

---

## Unlock order (recommended)

Goal: maximize automation and usefulness with the fewest changes.

### 1) Configure web discovery (Brave Search API)
Impact:
- Local Scene Analyzer can discover venues/promoters/event listings.
- Trend Watcher can discover sources beyond YouTube.
- Any “spider outward” agent becomes much more autonomous.

### 2) Install a supported browser OR use Browser Relay (Chrome extension)
Impact:
- Enables JS-heavy sites and login-required browsing (especially Instagram).
- Makes “IG trend research” and “local events via IG” feasible.

### 3) Establish a consistent secrets workflow
Impact:
- Safe key management for Groq/OpenAI/etc.
- Enables more integrations without leaking keys.

### 4) Finish the 0.4c corpus transcription backlog
Impact:
- Unlocks Framework Synthesizer outputs (Meta ads, short-form, release strategy).

### 5) Provide Nukage anchor tracks + constraints
Impact:
- Makes all strategy outputs tailored rather than generic.

### 6) Local Scene Analyzer: seed URLs/handles → first spider run
Impact:
- Quickly populates the venue/promoter/DJ map and surfaces near-term opportunities.

### 7) Decide “crate output” target
Impact:
- Enables Playlist/Crate Builder + Downloader to be practical (Spotify vs Rekordbox vs files).

### 8) Merch Ops read-only access
Impact:
- Enables store intelligence and merch ideation grounded in real sales data.

---

## Global blockers (affect many agents)

### Web discovery
- 🔴 **Search discovery not configured** (OpenClaw `web_search` tool requires Brave API key).
  - Preferred fix (no paid API): stand up / use a **SearXNG** instance and route discovery through it.
  - What I need from Tom: SearXNG base URL (and whether it’s private/LAN-only and whether it needs an API key or auth).
  - Note: until OpenClaw has a native `web_search` provider for SearXNG, we can still use it via a small helper script + `web_fetch` (HTML) or SearXNG’s JSON endpoint.

### Browser automation
- 🔴 **No supported browser installed on OpenClaw host** (OpenClaw `browser start` fails).
  - Impact: JS-heavy sites (Instagram, some ticketing sites) are hard to spider.
  - Fix: install Chromium/Chrome/Brave on host, or rely on manual capture.
- 🔴 **Browser control service unreachable at runtime** (agent saw: “Can’t reach the OpenClaw browser control service”).
  - Impact: even public sources can’t be navigated interactively to pull transcripts, logins, etc.
  - Fix: get `browser start` working on the host OR use Browser Relay (logged-in Chrome tab).

### Membership-gated sources (YouTube “Join”, paid communities)
- 🔴 **Members-only video access blocks extraction of tactics + timestamped quotes** (e.g., Musformation/Jesse Cannon channel members-only episodes).
  - Symptom: yt-dlp errors like “Join this channel…”; no `.vtt` captions available.
  - Impact: we can draft frameworks/playbooks, but can’t *verify* or properly cite without transcript/captions.
  - Fix options:
    - Provide authenticated cookies for an environment with membership access (preferred), then ingest `.vtt` captions.
    - Or: you manually export transcript / copy key sections → we cite what you provide.

### Instagram/TikTok scraping
- 🟡 **Platform hostile to scraping**.
  - Workaround A: manual capture (share links/screenshots) → OCR + summarization.
  - Workaround B: Browser Relay (logged-in Chrome tab) for guided browsing.

---

## Agent prereqs by role

### 1) MMKB Corpus Builder (My .4 Cents)
Status: 🟡
- ✅ Acast RSS feed discovered.
- ✅ Groq key configured (`/home/ai-pc/.openclaw/secrets/groq.txt`).
- 🟡 Needs reliable checkpointing + time (long episodes; many chunks).
- 🟡 Needs alerts/reporting cadence so progress is visible.

### 2) Framework Synthesizer
Status: 🟡
- Needs: enough transcripts completed (suggest: 10–15) to start robust synthesis.
- Nice-to-have: stable citation format (episode GUID + chunk index).

### 3) DJ Taste Profiler
Status: 🟡
- ✅ Can start from seed artists and YouTube mix ecosystem.
- 🟡 Best with your personal YouTube playlist(s) (stronger taste signal).

### 4) Trend Watcher (Taste-aligned)
Status: 🟡
- ✅ YouTube-based trend monitoring possible.
- 🔴 If Instagram is a primary source: blocked without browser relay or manual capture.

### 5) Playlist/Crate Builder
Status: 🟡
- Needs: definition of output format (Spotify playlist? Rekordbox crate? plain markdown list?)
- Needs: approval workflow.

### 6) Downloader / Library Manager
Status: 🟡
- ✅ yt-dlp available.
- 🔴 Needs: decision on storage location + licensing policy.
- 🔴 Needs: approval gating rules (never auto-download unapproved content).

### 7) Local Scene Analyzer (State College, PA)
Status: 🟡
- ✅ Skeleton directories created in KB.
- 🟡 Spidering is limited without web_search/browser.
- Needs: exact IG handles / URLs for seed venues and promoters OR Brave API key.
- Needs: definition of “high bar” opportunity criteria (gig vs collab vs networking).

### 8) Merch Ops Agent (WooCommerce + FluentCRM)
Status: 🔴
- Needs: read-only WooCommerce API key.
- Needs: FluentCRM access method (API/plugin credentials).
- Needs: POD provider selection (Printful/Printify/etc.) for autonomous fulfillment.
- Must remain approval-gated for publish/email actions.
