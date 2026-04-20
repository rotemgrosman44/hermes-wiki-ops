---
title: ILINDEX X Operator
created: 2026-04-10
updated: 2026-04-20
type: project
tags: [ilindex, x-operator, marketing, content-strategy, authority]
sources: []
---

# ILINDEX X Operator

## Mission
Operate the public `claw.ilindex` voice on X in a practical, builder-facing way.

## Output Target
- Follow the current harness packet for exact shortlist size and lane rules.
- Prefer Hebrew-first replies and return fewer items when the pool is weak.
- Do not pad with weak English items to satisfy an old fixed volume target.

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
- Official X tooling first: `xurl` for reads, search, and validation.
- Browser automation is the live publish/review surface only when the current harness packet explicitly allows it.
- `x-cli` remains fallback-only for allowed write shapes.

## Current diagnostics (2026-04-20)
- Recent runs show Gate B as the most reliable discovery/search/validation lane in this workspace.
- Gate A/browser has repeatedly landed on the X login/signup shell with `Something went wrong. Try reloading.` and should be treated as unavailable when that happens.
- Learning: when Gate A is blocked by missing CDP/login, keep discovery on Gate B and treat Gate C reply/quote as packet-blocked for the cycle.
- `x-cli` reply/quote can still 403 on non-engaged threads; do not treat that as a general auth failure.
- Use recent session summaries and the gate scorecard before each cycle.

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

## Current Auth Decision
- Official direction for this operator is xurl, not x-cli.
- Reason: the current Hermes WhatsApp runtime does not load X secrets automatically, and the current local secret file does not contain the full OAuth 1.0a access-token pair required by x-cli.
- x-cli remains fallback only if a complete token set exists.
- Draft-only testing should move to xurl-based user auth first, then return to WhatsApp operation.
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


## Dedicated Browser Lane
- Hermes uses a dedicated Chrome profile for X web operations.
- Canonical note: [[credentials/x-operator-browser-lane]]
- This is the preferred live-write lane until official API write auth is completed end to end.
