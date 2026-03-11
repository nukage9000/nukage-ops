#project/nukage #type/runbook #topic/funnel

# FluentCRM Lead Magnet Funnel (Fans-first)

See also: [`FUNNEL_FRAMEWORKS_SYNTHESIS.md`](./FUNNEL_FRAMEWORKS_SYNTHESIS.md) (frameworks + landing page/email checklists).

This runbook defines the canonical “lead magnet → nurture” funnel implemented in **FluentCRM Pro** (WordPress).

## Goal
Turn short-form attention into an owned list and eventually:
- repeat listeners
- followers
- show attendance
- paid supporters (music files, merch, tickets)

## Core CTA
> “Listen to the full track here.”

## Offer structure (recommended)
**Primary:** private listening link for the current sprint flip/track (listen-only if bootleg)

**Bonus (safe + yours):** an original track download / promoted release.

## Components

### 1) Opt-in form (FluentCRM)
**Fields:**
- Email (required)
- First name (optional but recommended)

**Tagging:**
- Tag: `lm:flip` (or more specific like `lm:flip:smack-talk`)
- Tag: `source:<platform>` (ig / tt / yt) if you can capture it

**Double opt-in:** optional; start without it for lower friction.

### 2) Thank-you page (WordPress)
Immediately after form submit.

Include:
- Heading: “You’re in.”
- The listening link (unlisted/private)
- Bonus original download link
- Optional: “Next drop” teaser (join/follow links)

**Safety note (bootlegs):** prefer listen-only links; avoid direct download links for bootlegs.

### 3) Automation (FluentCRM)
Trigger: Tag applied (e.g., `lm:flip`)

**Email 0 — Instant (send immediately)**
- Subject: “Your private link 🎧”
- Content:
  - Listening link
  - Bonus download
  - One CTA: “Reply with 1 word: harder / weirder / more melodic”

**Email 1 — +1 day**
- 30s behind-the-build story + 1 clip link
- CTA: follow on IG/TT/YT (one link hub)

**Email 2 — +3 days**
- “If you liked this, start here” (2–3 best links: Spotify/YouTube)
- CTA: save/follow

**Email 3 — +7 days**
- Invite: next drop / set debut / mailing list perk
- CTA: whitelist / reply

### 4) Metrics (weekly)
- Opt-ins per clip
- Opt-in conversion rate (visits → opt-in) if measurable
- Reply rate to Email 0 question
- Unsub rate

## Minimal operating procedure (weekly)
1) Pick the current flip/track + set the `lm:*` tag.
2) Ensure thank-you page link is correct.
3) Schedule 3 posts (Mon/Wed/Fri 12:15pm ET) with the single CTA.
4) Review new subs + replies once/week.

## Copy blocks (starter)

### Caption CTA (short)
“Want the full track? Link in bio → I’ll send it instantly.”

### Caption CTA (comment keyword)
“Comment ‘LINK’ and I’ll DM you the private listen.”

### Email 0 CTA question
“Reply with ONE word: harder / weirder / more melodic.”

## Naming conventions
- Tags: `lm:<magnet>` and optionally `lm:<magnet>:<campaign>`
- Pages: `/private-listen/` and `/download/` (or campaign-specific)

## Open questions for Tom (answer later)
- Where will listening be hosted (unlisted YT, SoundCloud private, etc.)?
- Do we want a separate funnel per flip, or a rolling funnel with rotating content?
