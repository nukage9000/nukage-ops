# Agent Blockers & Prereqs

This file tracks what each planned agent needs before it can run smoothly and safely.

Legend:
- ✅ ready
- 🟡 partial / can start with manual inputs
- 🔴 blocked

---

## Global blockers (affect many agents)

### Web discovery
- 🔴 **Brave Search API key not configured** (OpenClaw `web_search` tool errors).
  - Fix: create Brave Search API key + `openclaw configure --section web`.

### Browser automation
- 🔴 **No supported browser installed on OpenClaw host** (OpenClaw `browser start` fails).
  - Impact: JS-heavy sites (Instagram, some ticketing sites) are hard to spider.
  - Fix: install Chromium/Chrome/Brave on host, or rely on manual capture.

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
