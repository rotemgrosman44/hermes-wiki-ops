---
title: Default Remote Target
created: 2026-04-10
updated: 2026-04-10
type: decision
tags: [decision, hermes, bridge, authority]
sources: []
---

# Default Remote Target

## Decision
The default Git remote for the Hermes wiki is a separate private repository named `hermes-wiki-ops`.

## Why
- Keeps Hermes operational memory separate from Jarvis canon.
- Avoids mixing with upstream `hermes-agent` code.
- Preserves the bridge as the only approved Jarvis-Hermes handoff lane.

## Default Owner Shape
- User-owned private GitHub repository.
- `main` as default branch.
- `origin` as remote name.

## Allowed Content
- Hermes wiki structure
- templates
- playbooks
- approved decisions
- push-safe credential contracts

## Forbidden Content
- secrets
- `credentials/local/`
- Jarvis canon
- bridge drops
- raw exposed tokens

## Push Rule
If no explicit remote is provided, use `hermes-wiki-ops` as the default recommendation.
