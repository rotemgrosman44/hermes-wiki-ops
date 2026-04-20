---
title: Jarvis MAIN
created: 2026-04-17
updated: 2026-04-17
type: entity
tags: [identity, jarvis, authority, runtime, openclaw]
sources: []
---

# Jarvis MAIN

## Canonical Runtime
- Master operator lives on the Mac-side Jarvis/OpenClaw environment.
- Laptop visibility is through read-only mirrors and the separate local portal surface.

## Canonical Surface
- External portal reference from the laptop: `http://127.0.0.1:19101/chat?session=agent%3Amain%3Amain`
- Hermes dashboard may link to Jarvis, but it must not absorb Jarvis into Hermes runtime truth.

## Job
- Master operator and higher-order governor for Mac-side and Jarvis/OpenClaw execution.
- Receives bounded handoff bundles from Hermes through the bridge only.

## Hard Boundaries
- No direct Hermes-side write lane into `jarvis-canon`.
- No identity merge with Hermes main or the Telegram Twitter operator.

## Related
- [[concepts/protocols/canonical-identity-map]]
- [[projects/jarvis-bridge/jarvis-bridge]]
- [[playbooks/jarvis-bridge-handoff-contract]]
