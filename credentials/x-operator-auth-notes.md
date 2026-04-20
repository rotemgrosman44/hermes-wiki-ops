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
- Callback URL: `http://localhost:8080/callback`
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

## Current Blocker
- The active Hermes WhatsApp runtime does not load X credentials from the wiki-local secret file automatically.
- The current local X secret file is incomplete for x-cli:
  - X_ACCESS_TOKEN is blank
  - X_ACCESS_TOKEN_SECRET is blank
  - X_CLIENT_SECRET is also blank
- The current x-cli skill requires this exact set before read/write operations will work:
  - X_API_KEY
  - X_API_SECRET
  - X_BEARER_TOKEN
  - X_ACCESS_TOKEN
  - X_ACCESS_TOKEN_SECRET
- If the stored file uses X_CONSUMER_KEY / X_CONSUMER_SECRET, they must be mapped to X_API_KEY / X_API_SECRET for x-cli.

## Operational Note
- Paid X developer access alone is not enough for the current Hermes operator path.
- The current operator skill path is x-cli, which still depends on user access token material, not just app-level client credentials.
