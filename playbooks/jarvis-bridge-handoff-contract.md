---
title: Jarvis Bridge Handoff Contract
created: 2026-04-17
updated: 2026-04-17
type: playbook
tags: [playbook, bridge, jarvis, hermes, protocol, authority]
sources: []
---

# Jarvis Bridge Handoff Contract

## Purpose
Define the narrow, approved way Hermes prepares a handoff for Jarvis without writing directly into Jarvis canon.

## Use This Playbook When
- A validated Hermes result must be handed to Jarvis MAIN.
- The next step belongs to Mac-side authority or Jarvis/OpenClaw execution.
- Rotem explicitly asks for a bounded update package to Jarvis.

## Do Not Use This Playbook When
- The work remains inside Hermes-local runtime truth.
- The item is only a reminder to Rotem.
- The material is still unvalidated, noisy, or exploratory.
- The request would widen into direct edits under `jarvis-canon`.

## Required Package
- `status.json`
- `outbound.json`

## Optional Package
- `summary.md`

## Storage Rule
- Immutable source notes and packet material live under `wiki/raw/bridge-packets/`.
- Package files are created from `_templates/bridge-handoff-*`.
- No direct write lane to `/home/rotemg/work/jarvis-canon`.
- Google Drive is not a required transport surface in the canonical flow.

## Minimal Contract
- `status.json` states the handoff id, source runtime, target, validation state, and whether human approval is still required.
- `outbound.json` states the bounded payload, allowed next actions, blocked actions, evidence artifacts, and one next safe step.
- `summary.md` is human-readable and optional.

## Human Gate Rule
- If the bundle changes public action, authority, or business meaning, the package remains approval-gated until Rotem approves.

## Related
- [[projects/jarvis-bridge/jarvis-bridge]]
- [[playbooks/packet-intake]]
- [[playbooks/return-packaging]]
