# Blockers / Unlock Checklist (Tom)

This is the “make the bots smoother” checklist.

## 0) Quick context
Right now the main blockers to fully autonomous “spider” behavior are:
- No web search API key configured (so the agent can’t discover sources on its own)
- No browser automation available on the OpenClaw host (limits JS-heavy sites)
- Some sites block automated fetch (Cloudflare/Instagram)

---

## 1) Enable spider mode (Local Scene Analyzer)

### 1.1 Add Brave Search API key to OpenClaw (recommended)
**Why:** Lets the agent discover venues/promoters/events without you hand-feeding URLs.

**To do:**
1) Create a Brave Search API key (Brave Search API).
2) On the OpenClaw VM/host terminal:
   - `openclaw configure --section web`
   - set `BRAVE_API_KEY`

**Done when:** agent can successfully run `web_search` without “missing_brave_api_key”.

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
