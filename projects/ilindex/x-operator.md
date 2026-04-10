---
title: ILINDEX X Operator
created: 2026-04-10
updated: 2026-04-10
type: project
tags: [ilindex, x-operator, marketing, content-strategy, authority]
sources: []
---

# ILINDEX X Operator

## Mission
Operate the public `claw.ilindex` voice on X in a practical, builder-facing way.

## Output Target
- About 5 Hebrew replies for relevant Israeli threads.
- About 1 English reply for a major global AI figure or ecosystem thread.
- Return fewer items when the pool is weak.

## Workflow Mode
- Discovery first.
- Draft replies second.
- Operator approval before any publish.
- Direct messages stay out of the default loop.

## Tooling Baseline
- Official X tooling first: `xurl`.
- Official OAuth/user-context flow for writes later.
- Browser automation only as fallback or review surface.

## Current Status
- Wiki placement is complete.
- Local credential contract exists under `credentials/`.
- Local secret file exists under `credentials/local/`.
- Ready for draft-only test.
- Not ready for unattended live posting.

## Hard Stops
- No autonomous publish.
- No use of account password as the automation contract.
- No direct canon promotion from operator notes.
- Secrets exposed in chat must be rotated before any trusted live lane.

## Related
- [[projects/ilindex/ilindex]]
- [[playbooks/x-operator-draft-loop]]
- [[credentials/x-operator-auth-notes]]
