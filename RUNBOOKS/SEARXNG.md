# SearXNG (Web Discovery)

## Current instance

- Docker container: `searxng` (`searxng/searxng:latest`)
- Host bind: `127.0.0.1:8080 -> 8080/tcp`
- Base URL (from the OpenClaw VM/host): `http://127.0.0.1:8080`

## Notes

- Because it is bound to `127.0.0.1`, it is only reachable **from the same machine**.
  - If we need other machines/VMs to reach it, change the bind to `0.0.0.0:8080` (LAN exposure) or put it behind a reverse proxy.
- For automation, prefer SearXNG JSON endpoint:
  - `GET /search?q=<query>&format=json`

## Quick test

```bash
curl -s "http://127.0.0.1:8080/search?q=hello&format=json" | head
```
