---
title: X Operator Draft Loop
created: 2026-04-10
updated: 2026-05-02
type: playbook
tags: [playbook, x-operator, ilindex, marketing]
sources: []
---

# X Operator Draft Loop

## Standard Loop
1. Open a fresh search cycle.
2. Find relevant recent X threads.
3. Rotate search themes and keyword clusters.
4. Filter for relevance, freshness, diversity, and fit to `claw.ilindex`.
5. Draft custom replies.
6. Return shortlist plus drafts.
7. Ask one short learning question for the next cycle.
8. Wait for operator approval.
9. Publish only in a later approved phase.

## Memory Load Rule
- Normal operation should use [[projects/ilindex/x-operator-active-rules]] rather than broad history.
- Use [[projects/ilindex/x-operator-golden-examples]] only when reply quality needs calibration.
- Use [[projects/ilindex/x-operator-run-metrics]] and [[projects/ilindex/x-operator-learning-school]] only for diagnosis or deliberate improvement.
- Raw reports remain evidence, not default context.

## Freshness Rule
- Preferred: last 2 to 3 days.
- Warn when a target is older and still being considered.
- Skip stale threads unless they remain active and relevant.

## Diversity Rule
- Do not keep hitting the same users every cycle.
- Do not keep centering the same companies every cycle.
- If two candidates are similarly good, prefer the one that improves spread across the ecosystem.

## Search Rotation Rule
Rotate across themes such as:
- agents and autonomous workflows
- automation in real work
- onboarding and installation
- memory, files, permissions, and tools
- Israeli AI builder discourse
- major global AI lab or ecosystem threads

Keep the rotation long enough that the lane does not feel repetitive.

## Quality Rule
- Short, useful, operator-level replies.
- Hebrew first and Hebrew-source only for this operator.
- Do not draft Hebrew replies for English-only or non-Hebrew source/root/parent posts.
- No hype, no fake certainty, no repetitive templating.

## Return Shape
For each candidate, return only:
1. link
2. handle
3. draft reply
4. why this is good now

Do not include:
- long context summary
- confidence score
- security level

## Safety Rule
- Draft-first by default.
- DM scope is disabled in the default lane.
- If the candidate pool is weak, return fewer items and say so plainly.
- In a manual approved publish window, execute the approved numbered set silently through Gate A, preserve exact approved shape, verify each publish, and treat blocked-author reply surfaces as hard drops unless Rotem approves a new shape.

## Related
- [[projects/ilindex/x-operator]]
- [[projects/ilindex/x-operator-active-rules]]
- [[projects/ilindex/x-operator-golden-examples]]
- [[credentials/x-operator-auth-notes]]
- [[playbooks/authority-boundaries]]

## Auth Rule
- Current publish path: Gate A browser only.
- `xurl`, `x-cli`, and official API notes are diagnostic/legacy context only unless the current runbook explicitly re-enables them for read-only validation.
- Do not use API write paths for publish in this harness.
- If credentials or locations are missing, ask only for the current location, never for raw secret values.
