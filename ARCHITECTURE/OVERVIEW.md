# Architecture Overview

## Repos

### 1) nukage-ops (this repo)
- Planning docs
- Architecture decisions
- Runbooks (how to operate the system)

### 2) music-marketing-knowledgebase
- Corpus (scraped/transcribed content)
- Insights/frameworks
- Playbooks/SOPs

## Branching
- Agents commit to `agent-updates` branch in the KB repo.
- Humans review/merge PRs as needed.

## Alerting
- Telegram Alerts topic is the default destination for status reports.
