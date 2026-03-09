# Kanban Dashboard Idea (Agent-accessible)

## Motivation
Trello is currently used to organize songs, but we want a system that:
- supports **file attachments** (stems, bounces, clips, images)
- is easily **agent-accessible/read-write**
- avoids fragile UI automation / API key issues

## Proposed approach (start simple)
### Option 1 — File-backed Kanban + Unraid storage (recommended v0)
- Kanban board stores **metadata + pointers** to attachments.
- Attachments are stored on Unraid and mounted on the OpenClaw VM at `/mnt/ai-pc/`.
- Each card includes `attachments:` list of file paths (or SMB URLs).

Pros:
- reliable + auditable (git)
- no upload plumbing
- agents can directly access files via the mount

Cons:
- UI is basic unless we build a renderer.

### Option 2 — Kanban web UI with uploads to Unraid (upgrade)
- Small local app that supports drag/drop upload.
- Saves attachments to Unraid folders per-card.
- Generates thumbnails/waveforms.

Pros:
- Trello-like UX

Cons:
- more engineering/maintenance

## Suggested Unraid folder layout
- `/mnt/ai-pc/kanban/`
  - `songs/<slug>/` (stems/bounces/exports)
  - `clips/<date>/` (exports for Buffer)
  - `covers/<slug>/` (raw takes, comps)

## Board columns (draft)
- Ideas
- Sketch
- Drop-moment-ready
- Performance-template-ready
- Funnel-ready
- Scheduled
- Released
- Parked

## Tags/roles
- flip / VIP / Spotify / cover

## Next time
Decide whether to start with Option 1 or keep Trello and mirror key info.
