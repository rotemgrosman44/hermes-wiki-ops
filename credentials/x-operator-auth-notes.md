---
title: X Operator Auth Notes
created: 2026-04-10
updated: 2026-04-10
type: summary
tags: [credentials, x-operator, security, hermes]
sources: []
---

# X Operator Auth Notes

## Durable Non-Secret Contract
- App name: `ILINDEX Hermes Operator`
- Organization: `ILINDEX`
- Website URL: `https://ilindex.com/open-claw/`
- Callback URL: `http://127.0.0.1:8787/x/callback`
- Scope baseline: `tweet.read tweet.write users.read offline.access`
- App mode target: automated operator flow with approval-gated posting

## Local Secret Location
- `credentials/local/x-operator.env`

## Security Rule
- Keep live secrets in the local file only.
- Do not commit tokens, client secret, bearer tokens, or access tokens.
- Treat any secret pasted into chat or screenshots as exposed.
- Rotate exposed values before trusted live use.

## Current Readiness
- Enough structure exists for draft-only operator testing.
- Live posting still requires rotated secrets and an explicit publish gate.
- DM capability exists in permissions but is outside the default mission.

## Related
- [[projects/ilindex/x-operator]]
- [[credentials/README]]
- [[playbooks/x-operator-draft-loop]]
