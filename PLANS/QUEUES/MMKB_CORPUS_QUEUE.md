#project/nukage #type/queue

# MMKB Corpus Queue

Pull-based backlog for the **Corpus Builder**. Add items at the bottom.

Columns:
- status: TODO | DOING | DONE | BLOCKED
- type: podcast | youtube | article
- source: URL or ID
- notes: optional

---

## Queue

- status: DONE
  type: podcast
  source: https://shows.acast.com/my-point-4-cents-podcast/episodes/music-marketing-2026-insider-predictions
  notes: "0.4c (Acast) guid=695c64313edf36b7902dd7be — confirmed transcript exists"

- status: DONE
  type: podcast
  source: https://shows.acast.com/my-point-4-cents-podcast/episodes/how-black-veil-brides-built-their-fanbase
  notes: "0.4c (Acast) guid=694883dd3aa794d3c6b9a353 — confirmed transcript exists"

- status: DONE
  type: podcast
  source: https://shows.acast.com/my-point-4-cents-podcast/episodes/the-secrets-of-boosting-your-spotify-algortihm-w-luke-mansel
  notes: "0.4c (Acast) guid=694883be9ff9a1898696a6f3 — confirmed transcript exists"

- status: DONE
  type: youtube
  source: https://youtu.be/CExglfosZUM?si=pKRzAW91m56N80DN
  notes: "Captions + source note ingested → vaults/music-marketing-knowledgebase/11_SOURCES/Half/YouTube/Episodes/CExglfosZUM - if-you-want-a-real-music-career-in-2026-10-step-plan.md"

## Log

(append-only)

- 2026-03-09 12:52 EDT — Attempted Acast 0.4c batch transcription (--limit=3). Blocked: Groq transcription curl hung/stalled on guid=695c64313edf36b7902dd7be; run terminated; progress/failures updated; no new transcripts committed.
- 2026-03-10 06:00 EDT — Attempted Acast 0.4c batch transcription (--limit=3). Blocked: Acast media download rate-limited (HTTP 429) on all 3 items (guids 69252f85365dc3dd9c4e636f, 691be925b9580981599826a3, 6912e429c1ed8717c5d3984d). Progress notes updated; no transcripts generated.
- 2026-03-11 06:00 EDT — Attempted Acast 0.4c batch transcription (--limit=3). Blocked: Acast media download rate-limited (HTTP 429) on all 3 items (guids 68e561c3f513ad2b819c0690, 68db20ba7be17a7f01b77764, 68d21ba1325b3a0ac82df4e9). Progress notes updated; no transcripts generated.
- 2026-03-11 12:49 EDT — Ingested YouTube captions (CExglfosZUM) into MMKB vault + created source note for future synthesis.
- 2026-03-12 06:00 EDT — Attempted Acast 0.4c batch transcription (--limit=3). Blocked: Acast rate-limited (HTTP 429) on all 3 items (guids 68b7defe093397eb050cc784, 68b676ae70ab6f8350d2d6e9, 68ad39fbef1a5f8b368c04f4). Progress notes updated; no transcripts generated.
- 2026-03-13 06:00 EDT — Attempted Acast 0.4c batch transcription (--limit=3). Blocked: Acast rate-limited (HTTP 429) on all 3 items (guids 68954b74c952cf597835e4ac, 68918b5df3bc046081a05019, 688b04d3fc150bcf7fb59930). Progress notes updated; no transcripts generated.
- 2026-03-15 T17:08Z: MMKB Corpus: Acast batch limit=3 run executed; no new transcripts found. No transcripts dumped; no external posting.
- 2026-03-18 08:19 EDT — Daily corpus check. All 44/44 Acast transcripts present (100% complete). Marked 3 stale TODO queue items as DONE. No new work; no commit needed.
- 2026-03-19 08:28 EDT — Daily corpus run: `transcribe_acast_batch --limit=3` returned “Nothing to do” (corpus already complete). Progress timestamp updated in MMKB and committed (0e76754).
- 2026-03-20 09:06 EDT — Daily corpus run: `transcribe_acast_batch --limit=3` found no pending episodes (44/44 complete). Updated Acast progress notes; committed MMKB status update (1f74f5c). No blockers.
- 2026-03-21 12:12 EDT — Daily corpus run: `transcribe_acast_batch --limit=3` returned “Nothing to do” (44/44 complete). Progress timestamp updated and committed in MMKB (622e6da). No blockers.
- 2026-03-22 06:00 EDT — Daily corpus run: `transcribe_acast_batch --limit=3` returned "Nothing to do" (44/44 complete). Progress timestamp updated and committed in MMKB (9c98734). No blockers.
- 2026-03-23 08:55 EDT — Daily corpus run: `transcribe_acast_batch --limit=3` returned "Nothing to do" (44/44 complete). Progress timestamp updated and committed in MMKB (7a5a8e6). No blockers.
- 2026-03-24 06:00 EDT — Daily corpus run: `transcribe_acast_batch --limit=3` returned "Nothing to do" (44/44 complete). Progress timestamp updated and committed in MMKB (da9d748). No blockers.
- 2026-03-25 06:00 EDT — Daily corpus run: `transcribe_acast_batch --limit=3` returned "Nothing to do" (44/44 complete). Progress timestamp updated and committed in MMKB (244e6bb). No blockers.
- 2026-03-26 06:00 EDT — Daily corpus run: `transcribe_acast_batch --limit=3` returned "Nothing to do" (44/44 complete). Progress timestamp updated and committed in MMKB (bb71733). No blockers.
