---
title: X API Official Notes 2026-04-10
created: 2026-04-10
updated: 2026-04-10
type: summary
tags: [x-operator, diagnostics, security]
sources: ["https://docs.x.com/tools/xurl", "https://docs.x.com/x-api/direct-messages/lookup/quickstart"]
---

# X API Official Notes 2026-04-10

## Validated
- `xurl` is the official X CLI and is recommended for agent-friendly discovery and posting flows.
- `xurl auth` opens a browser OAuth flow and stores tokens locally after authorization.
- Direct Messages require authenticated user access tokens, not only app bearer tokens.

## Operational Consequence
- Hermes should use `xurl` first for discovery and approval-gated posting flows.
- DM should remain outside the default operator mission.
