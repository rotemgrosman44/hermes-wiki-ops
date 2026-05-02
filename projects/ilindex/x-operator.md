---
title: ILINDEX X Operator
created: 2026-04-10
updated: 2026-05-02
type: project
tags: [ilindex, x-operator, marketing, content-strategy, authority]
sources: []
---

# ILINDEX X Operator

## Mission
Operate the public `claw.ilindex` voice on X in a practical, builder-facing way.

## Runtime Authority
- Live runtime: `/home/rotemg/.hermes-twitter-operator`
- Durable learning memory: this Hermes wiki.
- Canonical operating rules: [[projects/ilindex/x-operator-active-rules]]
- Quality examples: [[projects/ilindex/x-operator-golden-examples]]
- Deep learning school: [[projects/ilindex/x-operator-learning-school]]
- Run evidence and timing: [[projects/ilindex/x-operator-run-metrics]]

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

## Memory Load Policy
- Normal runs load the current runbook and [[projects/ilindex/x-operator-active-rules]] only.
- Draft quality improvement may consult [[projects/ilindex/x-operator-golden-examples]].
- Diagnosis and deliberate improvement may consult [[projects/ilindex/x-operator-learning-school]] and [[projects/ilindex/x-operator-run-metrics]].
- Raw reports and old sessions are evidence, not default prompt context.

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
- Active direction for this operator is browser/web discovery and Gate A publish.
- Paid X API discovery is disabled while credits are unavailable.
- `x-cli` is not a publish lane for this harness.

## Current Status
- Wiki placement is complete.
- Local credential contract exists under `credentials/`.
- Local secret file exists under `credentials/local/`.
- Ready for bounded autonomous cron publish when Gate A is `publish_ready`, standing approval exists, and proof is written.
- Not ready for unattended multi-item posting or Gate C publish.

## Hard Stops
- No autonomous publish outside the standing one-item cron approval window or an explicitly approved manual publish window.
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
