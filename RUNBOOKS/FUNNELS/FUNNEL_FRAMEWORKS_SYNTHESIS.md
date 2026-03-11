# Funnel Frameworks Synthesis (Nukage / FluentCRM)

Purpose: distill the **most reusable funnel patterns** in the Music Marketing KB into **actionable checklists** that map cleanly to Nukage’s current stack: **short-form → landing pages (WP) → FluentCRM → follow-up**.

This doc is a synthesis (not a transcript). Each section cites its KB sources as **file path + heading**.

---

## 0) The core model (keep this invariant)

A funnel is a *sequence*, not a post.

**Cycle:** Attention → Conversation → Intrigue → Action

- **Attention:** short-form reach
- **Conversation:** DMs/comments/email replies (relationship step)
- **Intrigue:** context + stakes + proof (“why should I care?”)
- **Action:** click / opt-in / listen / buy

**Sources**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Adam Ivy - Music Selling Cycle (Attention → Conversation → Intrigue → Action).md` — “Core idea”, “Minimal viable cycle”
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - CTA Coverage System (Every Post Converts).md` — “Step 1) Choose ONE primary CTA for the week”, “Failure modes”

---

## 1) Minimum Viable Funnel (MVF) for Nukage (default)

Use this when you want a repeatable system that doesn’t require a blog and doesn’t break production momentum.

**MVF assets**
1. **One promise** (lead magnet)
2. **One CTA** (stable for 7 days)
3. **One landing page** (opt-in or click-through)
4. **One thank-you page** (delivery)
5. **One follow-up sequence** (4 emails is enough)

**MVF email spine (recommended)**
- **Email 0 (instant):** deliver the thing + one micro-commitment (“reply with 1 word…”) 
- **Email 1 (+1 day):** behind-the-build story + “follow here”
- **Email 2 (+3 days):** “start here” links (Spotify/YT) + save/follow CTA
- **Email 3 (+7 days):** invite to next drop / whitelist / soft support CTA

**Where this comes from**
- MVF + “one CTA” discipline: `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Lead Magnet Sprint Design (Musicians).md` — “Sprint rules (non-negotiables)”, “Step 4) Delivery workflow”
- Lead magnet specificity + low friction: `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Lead Magnets That Convert (Musicians).md` — “The conversion equation”, “Friction ladder”, “Failure modes”

---

## 2) Lead magnets: what actually converts (and what to pick)

### The conversion equation (use this to debug)
A lead magnet converts when it nails:
1) **Moment fit** (why now)
2) **Specific promise** (what they get)
3) **Low-friction next step** (single CTA)

If views are high but opt-ins are low, the magnet is usually: unclear / too much friction / wrong audience.

**Source**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Lead Magnets That Convert (Musicians).md` — “The conversion equation”

### Recommended Nukage magnet types (practical)
Pick based on what you want to attract:

1) **Access magnet** (highest conversion)
- “Private listen / early access / unreleased ID”
- Best when a clip is getting traction and you want to capture the spike.

2) **Utility magnet** (great for DJs/producers)
- 1-page checklist / transition cheat sheet / hook bank.

3) **Asset pack** (high perceived value)
- Tiny curated FX mini-pack + demo clips.

**Source**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Lead Magnets That Convert (Musicians).md` — “Lead magnet taxonomy”

### Friction ladder (start low; raise later)
From lowest to highest friction:
1) Comment keyword → DM link
2) DM keyword → link
3) Email opt-in → link
4) Email opt-in → confirm + tag
5) Application/survey

**Rule:** start at the lowest friction that still qualifies the right people.

**Source**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Lead Magnets That Convert (Musicians).md` — “Friction ladder”

---

## 3) Capture mechanics: DM-first vs email-first (and when)

### Option A — DM-first (fastest, easiest to start)
**Flow:** Short-form CTA → DM keyword → deliver link → ask for email (2nd DM)

**Why it works:** minimal friction; relationship starts immediately.

**Source**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Lead Magnet Sprint Design (Musicians).md` — “Step 0) Define the relationship step”, “Step 4) Delivery workflow (manual-friendly)”

### Option B — Comment-to-DM automation (scale without living in DMs)
**Flow:** Reel CTA (“Comment SINGLE…”) → ManyChat DM delivers link → (optional) DM asks for email later

**Operating rule:** keep the DM short; goal is click/opt-in, not a conversation.

**Source**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - ManyChat Comment-to-DM Lead Capture.md` — “Setup (minimum viable)”, “Operating rules”, “Failure modes”

### Option C — Email-first (best for owned list + FluentCRM reporting)
**Flow:** Short-form CTA → opt-in landing page → thank-you page delivery → Email 0 instant

**Source (manual→tooling upgrade path)**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - Spreadsheet Email List MVP (Content → List).md` — “Weekly upgrade path”

---

## 4) Landing pages (WP): checklists that match the frameworks

Two pages matter:

### A) Opt-in landing page (capture)
**Goal:** convert a cold click into an email/SMS/lead tag.

**Checklist**
- [ ] One-sentence **specific promise** (matches the short-form CTA)
- [ ] One primary action (form submit / button)
- [ ] Minimal distractions (no extra CTAs)
- [ ] Trust cues (optional): “instant delivery”, “no spam”, “unsubscribe anytime”
- [ ] If running ads: pixel fires on **ViewContent** (page load) and **Lead** (form submit) 

**Why this is the checklist:** “one promise / one CTA / low friction.”

**Sources**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Lead Magnets That Convert (Musicians).md` — “The conversion equation”, “Failure modes”
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - CTA Coverage System (Every Post Converts).md` — “Choose ONE primary CTA for the week”
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Meta-Ads.md` — “Optimize for conversions, not traffic”, “Landing page + pixel is non-negotiable for cold”

### B) Thank-you page (delivery)
**Goal:** deliver immediately and set expectation for the relationship.

**Checklist**
- [ ] “You’re in” confirmation
- [ ] Deliver the asset/link **above the fold**
- [ ] One micro-commitment prompt (reply/DM prompt or “start here”)
- [ ] Optional: secondary link (Spotify/YT profile) only if it doesn’t distract from delivery

**Source (delivery simplicity)**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Lead Magnet Sprint Design (Musicians).md` — “Sprint rules (non-negotiables)” (#3 “One delivery link”)

---

## 5) Follow-up systems (email + DM) that don’t feel spammy

### Email: the “4-touch” nurture spine (recommended)
Use the MVF spine above, but keep these rules:

**Rules**
- One primary CTA per email (don’t split attention)
- Allow one micro-CTA: “reply with one word” (engagement + signal)

**Sources**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - CTA Coverage System (Every Post Converts).md` — “Failure modes” (multiple CTAs)
- (Existing Nukage ops implementation) `/home/ai-pc/.openclaw/workspace/nukage-ops/RUNBOOKS/FUNNELS/FluentCRM-LeadMagnet-Funnel.md` — “Automation (FluentCRM)”

### DM follow-up: ethical cadence + mini-CRM
If you’re doing manual DM outreach (collabs, creator magnets), use a real cadence so you don’t chase.

**Cadence (default)**
- Day 0 initial
- Day 2 bump
- Day 7 new value
- Day 21 close loop

**Rule:** max 3 follow-ups unless they re-engage.

**Source**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Nukage - Follow-up Cadence + Mini-CRM for DMs.md` — “Follow-up cadence (default)”, “Mini-CRM (minimum viable)”

---

## 6) FluentCRM implementation checklist (copy/paste build plan)

Use this when you’re building/duplicating funnels inside WordPress.

### Tags (minimum)
- [ ] `lm:<magnet>` (e.g. `lm:private-listen`)
- [ ] `source:<platform>` when possible (`source:ig`, `source:tt`, etc.)

### Automation (minimum)
Trigger: Tag applied (`lm:*`)
- [ ] Email 0 (instant delivery + reply prompt)
- [ ] Email 1 (+1 day)
- [ ] Email 2 (+3 days)
- [ ] Email 3 (+7 days)

### Weekly ops
- [ ] 7 days = 1 CTA (stable)
- [ ] Measure: opt-ins per CTA post, reply rate, unsub rate

**Sources**
- `/home/ai-pc/.openclaw/workspace/nukage-ops/RUNBOOKS/FUNNELS/FluentCRM-LeadMagnet-Funnel.md` — “Tagging”, “Automation (FluentCRM)”, “Minimal operating procedure (weekly)”
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Lead Magnet Sprint Design (Musicians).md` — “Sprint rules (non-negotiables)”, “Measurement (weekly review, 15 min)”

---

## 7) Metrics scoreboard (what to look at weekly)

Keep it boring and consistent.

**Top-of-funnel**
- Views/reach on CTA posts (attention)

**Relationship step**
- Keyword comments / DMs per 1,000 views
- Email opt-ins per 1,000 views

**Landing page** (if measurable)
- Landing page conversion rate

**Email**
- Reply rate to Email 0 prompt
- Unsub rate

**Ad-specific (if running Meta)**
- Cost per conversion (primary)

**Sources**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - CTA Coverage System (Every Post Converts).md` — “Track CTA coverage + action rate”
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - ManyChat Comment-to-DM Lead Capture.md` — “Metrics (weekly)”
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Meta-Ads.md` — “Use cost per result as the control knob”

---

## 8) Common failure modes (diagnostics)

- **Multiple CTAs** per post/email → lower action.
- **Vague promise** (“free pack”) → make it concrete.
- **No next step after DM** → deliver link + one instruction.
- **Collecting emails but never talking to them** → no relationship ladder.

**Sources**
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - CTA Coverage System (Every Post Converts).md` — “Failure modes”
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/FRAMEWORKS/Lead Magnets That Convert (Musicians).md` — “Failure modes (what kills conversion)”
- `/home/ai-pc/.openclaw/workspace/vaults/music-marketing-knowledgebase/PLAYBOOKS/Adam Ivy - Spreadsheet Email List MVP (Content → List).md` — “Failure modes”

---

## 9) Quick-start: pick one funnel this week

If you only do one thing:

1) Pick a magnet: **Private listen link** (Access magnet)
2) Pick one CTA for 7 days: “Link in bio → get the private link instantly”
3) Build:
- Opt-in page
- Thank-you page with private link
- FluentCRM automation (Email 0/1/2/3)
4) Post 3 shorts this week with the same CTA.

Then iterate.

(Implementation details live in the existing runbooks in this folder.)
