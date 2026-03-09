# Blockers / Unlock Checklist (Tom)

This is the “make the bots smoother” checklist.

## 0) Quick context
Right now the main blockers to fully autonomous “spider” behavior are:
- No web search API key configured (so the agent can’t discover sources on its own)
- Browser automation isn’t currently usable (no supported browser installed *and/or* browser control service unreachable), which limits JS-heavy sites and transcript extraction.
- Some sites block automated fetch (Cloudflare/Instagram)

---

## 1) Enable spider mode (Local Scene Analyzer)

### 1.1 Use SearXNG for web discovery (recommended)
**Why:** Lets the agent discover venues/promoters/events without you hand-feeding URLs—without paying for Brave.

**To do:**
1) Provide the SearXNG base URL (e.g., `https://search.yourdomain.com`).
2) Confirm access:
   - Is it reachable from the OpenClaw VM/host?
   - Is it public, LAN-only, or behind auth?
3) Implement a tiny helper (script or tool wrapper) that queries SearXNG’s JSON endpoint and returns top results (title/url/snippet).

**Done when:** agent can run a “search” step (via SearXNG) and get back 5–10 URLs reliably.

**Note:** OpenClaw’s built-in `web_search` tool is Brave-only today; SearXNG will be a parallel path unless/until we wire it into OpenClaw config.

### 1.2 (Optional) Install a supported browser on the OpenClaw host
**Why:** Helps with JS-heavy sites and interactive navigation.

**To do:**
- Install one of: Chrome / Chromium / Brave / Edge.

**Done when:** `browser start` works (OpenClaw browser tool can launch).

### 1.3 Seed links (fastest immediate unlock)
Even without web search, the agent can spider from exact URLs/handles.

**Send these links/handles to OpenClaw:**
- Basement Night Spot (URL / IG)
- Stage West (URL / IG)
- Sharkies (URL / IG)
- Zeno’s (URL / IG)
- Three Dots (URL / IG)
- Manny’s (URL / IG)
- GORINTO Productions — exact Instagram @handle
- Silly Goose — exact Instagram @handle
- Spaces In Between Productions — website/IG

---

## 2) Transcription stability / costs

### 2.1 Groq transcription
- Key file exists: `/home/ai-pc/.openclaw/secrets/groq.txt`
- Model: `whisper-large-v3-turbo`

**To do (optional):**
- Check Groq dashboard for rate/quota if you notice slowdowns.

---

## 3) Alerts organization

**Why:** Keep status spam out of your DM.

**To do (optional):**
- Create more Telegram topics (e.g. "Transcription", "DJ Research", "Local Scene")
- Send OpenClaw the topic IDs so each agent can report to the right place.

---

## 4) Make DJ/market research more specific to Nukage

**To do:**
Send 1–3 “anchor tracks” (released links or unreleased names), with a one-line descriptor each:
- BPM/energy/vibe

**Why:** Lets the agents map scenes/opportunities to *your* sound instead of generic clusters.

---

## Notes
- ChatGPT Plus does NOT cover OpenAI API usage. If we ever use OpenAI API again, set a hard spend limit.
- Prefer secrets in files under `/home/ai-pc/.openclaw/secrets/` with `chmod 600`.
