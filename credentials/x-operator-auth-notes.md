---
title: X Operator Auth Notes
created: 2026-04-10
updated: 2026-05-02
type: summary
tags: [security, x-operator, hermes]
sources:
  - /home/rotemg/.hermes-twitter-operator/control/twitter-operator/HERMES_TWITTER_GATE_CONTRACT.md
  - /home/rotemg/.hermes-twitter-operator/control/twitter-operator/HERMES_TWITTER_SIMPLE_RUNBOOK.md
---

# X Operator Auth Notes

## Current Runtime Decision
The dedicated Twitter operator is browser-first and Gate A only for publish.

## Active Credential Surface
- Gate A browser/login contract: `/home/rotemg/.hermes-twitter-operator/credentials/x-web.env`
- Required non-secret key names in that file: `X_LOGIN_EMAIL`, `X_LOGIN_HANDLE`, `X_LOGIN_PASSWORD`
- Secrets stay local. Never paste raw X credentials into Telegram, Wiki pages, bridge packets, or committed notes.

## Publish Authority
- Publish path: Gate A live browser only.
- Manual publish requires Rotem's explicit numbered approval.
- Cron has standing approval for at most one strongest eligible Hebrew item per scheduled run.
- Success requires proof: direct X URL, tweet id, or clear browser/profile proof.

## Out Of Default Scope
- DM operations are outside the default operator mission.
- `xurl`, `x-cli`, official X app keys, and API write attempts are diagnostic/legacy context only in the current harness.
- Do not spend normal runs on disabled or paid X API routes.
- Do not use x-cli/API write paths to bypass Gate A.

## Security Rule
- Keep live secrets only in local credential files.
- Treat any secret pasted into chat, screenshots, or reports as exposed and rotate before trusted use.
- If a credential location is missing, ask only for the current location, not for raw values.

## Related
- [[projects/ilindex/x-operator]]
- [[projects/ilindex/x-operator-active-rules]]
- [[credentials/x-operator-browser-lane]]
