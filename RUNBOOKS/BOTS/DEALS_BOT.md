# Deals Bot — Spec (v1)

#project/nukage #type/runbook #topic/automation

## Goal
Monitor selected sources for “needs immediate attention” deals and ping Tom on Telegram only when a listing matches strict criteria.

## v1 Target
- Item: **Ableton Move**
- All-in max: **$450** (price + shipping + tax if present; tax is often unknown until checkout)
- Cadence: **every 6 hours**, 24/7

## Next tracked item (queued)
- Item: **Teenage Engineering OP‑1 (original)**
- All-in max: **$800**
- Sources: eBay + Keepa (same pipeline)

## v1 Sources
- eBay (RSS/search)
- Keepa (Amazon tracking) → AgentMail bridge → Telegram

## Current implementation (v1)
- Script: `~/.openclaw/workspace/bin/deals-bot.mjs`
- State: `~/.openclaw/state/deals-bot.json`
- Systemd timer:
  - `nukage-deals-bot.timer` (OnBootSec=10m, OnUnitActiveSec=6h, Persistent=true, RandomizedDelaySec=15m)
  - `nukage-deals-bot.service`

### Keepa → Telegram bridge
- Keepa alerts go to: `nukagedeals@agentmail.to`
- AgentMail API key: `~/.openclaw/secrets/agentmail.txt`
- Deals bot reads newest inbox messages and forwards matches to Telegram DM.

## Alert format (normalized)
- **[DEAL] Ableton Move**
- Source: eBay | Amazon (Keepa)
- Price: $___ (all-in estimate if available)
- Link: <url>
- Why: matched ≤ $450

## Known constraints
- eBay: RSS gives price + shipping; tax is unknown until checkout.
- Keepa: email parsing is best-effort; may need tuning once real alerts arrive.
- Reverb: blocked by Cloudflare challenge from this host (needs alternative method).

---

## Next iteration ideas (v2+)

### 1) Wishlist-driven (multiple items)
- Add `nukage-ops/PLANS/QUEUES/DEALS_WISHLIST.yaml` (or .md) with multiple items, thresholds, preferred sources, and optional locations.
- Deals bot loops through wishlist items.

### 2) Better Keepa parsing + dedupe
- Parse ASIN / condition (Renewed/Used/New) from Keepa messages.
- Dedupe by Keepa alert id / ASIN.

### 3) Telegram formatting polish
- Include urgency cues ("BIN", "Ends in X hours")
- Inline buttons (if supported) to open listing

### 4) Reverb support
- If we can’t fetch Reverb directly, options:
  - Use Reverb API (if available)
  - Use browser-authenticated fetch with cookies
  - Use email alerts from Reverb into AgentMail, same as Keepa

### 5) Quiet hours / escalation tiers (optional)
- Keep 24/7 checks, but suppress non-urgent alerts at night unless “must buy now”.

### 6) Logging + dashboard
- Append alert log entries to `nukage-ops/PLANS/LOGS/DEALS_BOT_LOG.md`.
- Add counts + last run status to a future dashboard.
