# Deals Bot — Spec (v1)

#project/nukage #type/runbook #topic/automation

## Goal
Monitor selected sources for “needs immediate attention” deals and ping Tom on Telegram only when a listing matches strict criteria.

## v1 Target
- Item: **Ableton Move**
- All-in max: **$450** (price + shipping + tax if present)
- Cadence: **every 6 hours**, 24/7

## Sources
### v1
- eBay (RSS/search)
- Keepa (Amazon tracking) → bridge alerts into Telegram

### later
- Reverb (blocked by CF challenge from this host; needs alternative approach)
- Craigslist, FB Marketplace (harder)

## Keepa → Telegram bridge
- Keepa alerts go to: `nukagedeals@agentmail.to`
- AgentMail credential: `~/.openclaw/secrets/agentmail.txt` (token)
- Bot reads incoming Keepa alert(s), extracts:
  - item
  - price
  - link
  - condition (renewed/used/new)
- Bot sends normalized Telegram alert message.

## Alert format (normalized)
- **[DEAL] Ableton Move**
- Source: (eBay | Amazon/Keepa)
- Price: $___ (all-in est)
- Link: <url>
- Why: matched ≤ $450 (and condition ok)

## Open questions / requirements
- AgentMail access method (IMAP/SMTP vs HTTP API/webhook) needed to read incoming Keepa alerts.
- Keepa alert filtering: forward only matching alerts (recommended).
