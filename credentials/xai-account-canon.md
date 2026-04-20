---
title: xAI And X Account Canon
created: 2026-04-11
updated: 2026-04-11
type: summary
tags: [xai, x, identity, billing, canon, ilindex]
sources: []
---

# xAI And X Account Canon

## Validated
- Primary human root email is `grosmanrotem@gmail.com`.
- x.ai invitation mail reached `grosmanrotem@gmail.com`.
- X Developer Platform receipt for `$25.00` reached `grosmanrotem@gmail.com`.
- Hostinger verification mails reach `grosmanrotem@gmail.com`.
- ILINDEX / Open Claw outbound mail currently sends from `grosmanrotem@gmail.com`.
- The local `XAI_API_KEY` already works against `https://api.x.ai/v1/models`.
- The x.ai management key can list team API keys for team `fb9bd7e4-a9bc-453b-998c-b8467061c3a0`.

## Important Separation
- `x.ai` and `X Developer Platform` are not the same surface.
- `x.ai` key management controls Grok / x.ai runtime access.
- `X Developer Platform` billing controls X API access for posting / reading on X.
- Do not merge their credentials into one env file.

## Canonical Ownership Plan
- Human root owner:
  - email: `grosmanrotem@gmail.com`
  - recovery priority: private phone + passkey
  - purpose: billing owner, recovery owner, console owner
- Apple / device identity:
  - keep `RotemGrossman@icloud.com` as Apple / device identity only unless a later migration proves otherwise
  - do not use it as the main SaaS billing root by default
- Bot / operator identity:
  - `workflowbot@icloud.com` may remain a bot-login identity for the X web operator only
  - it should not become the billing owner for x.ai, Hostinger, or Google
- Legacy auxiliary identity:
  - `workflowrotem@outlook.com` is currently entangled with Meta and Google recovery flows
  - keep it as temporary recovery only until each linked service is re-pointed

## Current Drift
- `workflowbot@icloud.com` is stored as the X operator account email in the local operator env files.
- `workflowrotem@outlook.com` appears in live Meta / Facebook / Instagram flows and as a recovery email for `grosmanrotem@gmail.com`.
- The current docs and local credentials reflect at least two operator-email lanes.

## Canonical Secret Locations
- x.ai runtime:
  - `/home/rotemg/wiki/credentials/local/xai.env`
- x.ai management:
  - `/home/rotemg/wiki/credentials/local/xai-management.env`
- X API / operator:
  - `/home/rotemg/wiki/credentials/local/x-operator.env`
- X web login lane:
  - `/home/rotemg/wiki/credentials/local/x-web.env`

## Current x.ai Key Map
- `HERMES`
  - redacted key: `xai-...cwEI`
  - status: active
  - local match: matches the current local `XAI_API_KEY` suffix
  - intended role: Hermes runtime canonical inference key
- `jarvis new`
  - redacted key: `xai-...paxS`
  - status: active
  - intended role: legacy / review before keeping
- `jarvis2`
  - redacted key: `xai-...KOly`
  - status: active
  - intended role: legacy / review before keeping
- `jarvis`
  - redacted key: `xai-...MkWm`
  - status: active
  - note: narrower ACL set than the newer broad model keys

## Consolidation Rule
- Keep `HERMES` as the default x.ai runtime key unless a later owner decision replaces it.
- Do not disable legacy keys until the consuming machine or script is identified.
- After usage mapping is complete, retire unused `jarvis*` keys one by one from the management console.

## Machine Note
- Current validated Windows / WSL host is `DESKTOP-20AA9PG`.
- No live SSH host config for the Mac is present on this machine right now.
- Jarvis canon docs still point to a separate macOS managed browser lane at `/Users/rotemgrosman/.openclaw-mac-managed-browser-node`.

## Decision
- Make `grosmanrotem@gmail.com` the canonical owner for x.ai, X billing, Hostinger, Google, and ILINDEX admin.
- Keep bot identities scoped to operator use only.
- Treat all other emails as transitional until migrated.
