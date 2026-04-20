---
title: Hermes Code Remote Authority
created: 2026-04-20
updated: 2026-04-20
type: decision
tags: [decision, hermes, git, repo-authority]
sources:
  - /home/rotemg/.hermes/control/hermes-canonical-surfaces.md
  - /home/rotemg/.hermes/control/runbooks/hermes-maintenance-belt-2026-04-17.md
---

# Hermes Code Remote Authority

## Decision

Hermes customized code must be preserved in a Rotem-owned private repository named `hermes-agent-rotem`.

## Remote Model

- `origin`: `rotemgrosman44/hermes-agent-rotem`
- `upstream`: `NousResearch/hermes-agent`
- first private branch: `codex/hermes-rotem-laptop-2026-04-20`

## Why

- Nous remains the vendor source for upstream updates.
- Rotem-specific Web UI, voice, tools, onboarding, and operator patches must not live only as dirty install patches.
- Jarvis canon stays separate and must not receive Hermes code or Hermes wiki content.

## Push Boundary

Push only code, docs, tests, and push-safe examples.

Never push runtime secrets, auth files, sessions, pairing state, credentials, logs, caches, state databases, browser sessions, `node_modules`, `venv`, or bridge drops.

## Current Blocker

The laptop currently has no authenticated GitHub CLI/token path for creating or pushing to private repositories from WSL. The safe next step is to create the private GitHub repositories or authenticate `gh`, then push the prepared local branches.
