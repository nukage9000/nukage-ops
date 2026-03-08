# Secrets / API keys

Principles:
- Never commit secrets.
- Store secrets in `/home/ai-pc/.openclaw/secrets/` with `chmod 600`.

Current known keys:
- Groq transcription key: `/home/ai-pc/.openclaw/secrets/groq.txt`
- OpenAI key (optional/fallback): `/home/ai-pc/.openclaw/secrets/openai_mmkb_transcribe_key.txt`
