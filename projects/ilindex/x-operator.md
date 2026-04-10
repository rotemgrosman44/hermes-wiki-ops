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

## Selection Priorities
- Prefer diverse users and companies across cycles.
- Avoid over-targeting the same accounts unless the thread is clearly the best fit.
- Prefer threads over standalone posts when the thread gives enough context for a strong reply.
- Rotate search themes across cycles so the lane does not collapse into one repeated keyword cluster.

## Tooling Baseline
- Official X tooling first: `xurl`.
- Official OAuth/user-context flow for writes later.
- Browser automation only as fallback or review surface.

## Output Contract
Return only bottom-line decision material:
1. Link to the thread or post.
2. Account name or handle.
3. Draft reply.
4. One short line: why this is good now.

Do not return:
- confidence labels
- security/readiness labels
- long context summaries

After the shortlist, ask one short learning question that helps improve the next cycle.

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
