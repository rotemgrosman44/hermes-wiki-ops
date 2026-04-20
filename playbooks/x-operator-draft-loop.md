---
title: X Operator Draft Loop
created: 2026-04-10
updated: 2026-04-10
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
- Hebrew first for Israeli threads.
- English for global AI figures or English-native threads.
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

## Related
- [[projects/ilindex/x-operator]]
- [[credentials/x-operator-auth-notes]]
- [[playbooks/authority-boundaries]]

## Auth Rule
- Preferred auth path: xurl with official user-context auth.
- Do not treat app-only keys or client credentials as sufficient for the full operator loop.
- x-cli is not the default path for this Hermes lane unless X_API_KEY, X_API_SECRET, X_BEARER_TOKEN, X_ACCESS_TOKEN, and X_ACCESS_TOKEN_SECRET are all present and verified.
- If Hermes is running from WhatsApp, finish auth outside the chat first, then return to the draft loop.
