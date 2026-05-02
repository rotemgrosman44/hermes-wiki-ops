---
title: X Operator Dedicated Browser Lane
created: 2026-04-10
updated: 2026-05-02
type: summary
tags: [x-operator, hermes, runtime, security]
sources:
  - /home/rotemg/.hermes-twitter-operator/control/twitter-operator/HERMES_TWITTER_GATE_CONTRACT.md
  - /home/rotemg/.hermes-twitter-operator/scripts/twitter_operator_status.py
---

# X Operator Dedicated Browser Lane

## Current Decision
Hermes Twitter Operator uses a dedicated Gate A Chrome profile for X web operations.

## Runtime Truth
- Runtime root: `/home/rotemg/.hermes-twitter-operator`
- Launcher: `/home/rotemg/.hermes/control/scripts/start-x-operator-browser.ps1`
- Gate A credential contract: `/home/rotemg/.hermes-twitter-operator/credentials/x-web.env`
- Windows Chrome profile: `C:\Users\user\AppData\Local\Hermes\twitter-operator-clean-chrome`
- WSL CDP proxy: `http://172.22.240.1:9225`
- Browser surface is checked by `/home/rotemg/.hermes-twitter-operator/scripts/twitter_operator_status.py`

## Operational Rule
- Gate A is the only publish lane.
- The operator attaches to the dedicated Chrome/CDP lane and reuses its authenticated X session.
- A reachable browser is not enough: publish readiness requires a logged-in X page, usable composer/reply controls, viewport measurement, and proof after send.
- If the browser is narrow, cropped, or laggy, use DOM-based targeting instead of screenshot positioning.

## Legacy Notes
Older D-drive launcher paths and direct `127.0.0.1:9223` assumptions are legacy diagnostics only. They are not the active authority for this WSL Twitter operator. The active WSL-facing endpoint is the CDP proxy on `172.22.240.1:9225`.

## Related
- [[projects/ilindex/x-operator]]
- [[projects/ilindex/x-operator-active-rules]]
- [[entities/systems/hermes-twitter-operator]]
