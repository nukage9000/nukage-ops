# MMKB Corpus Queue

Pull-based backlog for the **Corpus Builder**. Add items at the bottom.

Columns:
- status: TODO | DOING | DONE | BLOCKED
- type: podcast | youtube | article
- source: URL or ID
- notes: optional

---

## Queue

- status: TODO
  type: podcast
  source: https://shows.acast.com/my-point-4-cents-podcast/episodes/music-marketing-2026-insider-predictions
  notes: "0.4c (Acast) guid=695c64313edf36b7902dd7be"

- status: TODO
  type: podcast
  source: https://shows.acast.com/my-point-4-cents-podcast/episodes/how-black-veil-brides-built-their-fanbase
  notes: "0.4c (Acast) guid=694883dd3aa794d3c6b9a353"

- status: TODO
  type: podcast
  source: https://shows.acast.com/my-point-4-cents-podcast/episodes/the-secrets-of-boosting-your-spotify-algortihm-w-luke-mansel
  notes: "0.4c (Acast) guid=694883be9ff9a1898696a6f3"

## Log

(append-only)

- 2026-03-09 12:52 EDT — Attempted Acast 0.4c batch transcription (--limit=3). Blocked: Groq transcription curl hung/stalled on guid=695c64313edf36b7902dd7be; run terminated; progress/failures updated; no new transcripts committed.
- 2026-03-10 06:00 EDT — Attempted Acast 0.4c batch transcription (--limit=3). Blocked: Acast media download rate-limited (HTTP 429) on all 3 items (guids 69252f85365dc3dd9c4e636f, 691be925b9580981599826a3, 6912e429c1ed8717c5d3984d). Progress notes updated; no transcripts generated.
- 2026-03-11 06:00 EDT — Attempted Acast 0.4c batch transcription (--limit=3). Blocked: Acast media download rate-limited (HTTP 429) on all 3 items (guids 68e561c3f513ad2b819c0690, 68db20ba7be17a7f01b77764, 68d21ba1325b3a0ac82df4e9). Progress notes updated; no transcripts generated.
