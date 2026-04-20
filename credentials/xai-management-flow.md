---
title: xAI Management Flow
created: 2026-04-11
updated: 2026-04-11
type: runbook
tags: [xai, management, flow, credentials]
sources: []
---

# xAI Management Flow

## Purpose
Use this flow for x.ai admin operations only:
- list team API keys
- create or disable team API keys
- inspect team-level ownership state

Do not use this flow for normal model inference.

## Local Files
- runtime inference key:
  - `/home/rotemg/wiki/credentials/local/xai.env`
- management key:
  - `/home/rotemg/wiki/credentials/local/xai-management.env`

## Safe Validation
```bash
set -a
source /home/rotemg/wiki/credentials/local/xai-management.env
set +a

curl -fsS \
  -H "Authorization: Bearer $XAI_MANAGEMENT_KEY" \
  "$XAI_MANAGEMENT_API_URL/auth/teams/$XAI_TEAM_ID/api-keys"
```

## Runtime Validation
```bash
set -a
source /home/rotemg/wiki/credentials/local/xai.env
set +a

curl -fsS \
  -H "Authorization: Bearer $XAI_API_KEY" \
  "$XAI_BASE_URL/models"
```

## Rule
- `XAI_MANAGEMENT_KEY` creates and governs runtime keys.
- `XAI_API_KEY` is what Hermes or scripts should actually use for model calls.
- Never point Hermes runtime at the management key.
