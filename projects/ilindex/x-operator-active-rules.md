---
title: X Operator Active Rules
created: 2026-05-02
updated: 2026-05-02
type: playbook
tags: [ilindex, x-operator, playbook, runtime, content-strategy]
sources:
  - /home/rotemg/.hermes-twitter-operator/control/twitter-operator/HERMES_TWITTER_SIMPLE_RUNBOOK.md
---

# X Operator Active Rules

## Purpose
This is the short rule sheet the Hermes Twitter Operator may load on every normal run.

## Runtime Truth
- Runtime root: `/home/rotemg/.hermes-twitter-operator`
- Control surface: Telegram and Mission Control for the Twitter Operator only.
- Durable learning: Hermes wiki, starting from [[projects/ilindex/x-operator]].
- Do not use Jarvis, bridge, Meta/Facebook, or OpenClaw as runtime authority.

## Normal Run Budget
- Manual BEACON/HUNTER/list requests run in fast shortlist mode.
- Return 2-4 grounded candidates or a clear blocker within 6-8 minutes.
- Stop at 25-30 focused tool steps.
- If compression or continuation starts during manual discovery, return partial candidates or `blocked_by_iteration_budget`; do not keep digging.

## Search And Source Rules
- Search latest Hebrew X sources first.
- Candidate source/root/parent must be mainly Hebrew.
- No English fallback and no Hebrew reply to a non-Hebrew target.
- Drop blocked accounts, reply-restricted targets, stale posts, duplicate authors, recently touched authors, and weak-fit political/noisy results.
- Use live X browser, built-in web search, Tavily, Brave, and Exa as available non-paid search surfaces.
- Do not spend a run on disabled or paid X API routes.

## Lane Rules
- `BEACON`: useful knowledge/update/context; no link by default.
- `HUNTER`: real help, implementation, installation, workflow, lecture, or workshop intent; CTA allowed when explicit.
- `COMPETITOR`: educator/course/speaker/direct peer; no commercial CTA.
- `MEDIA-BEACON`: only with approved media from the authorized media library.

## Publish Rules
- Gate A browser is the only publish lane.
- Manual publish requires Rotem's explicit numbered approval.
- Cron may publish at most one strongest item under standing approval.
- Preserve approved text and shape exactly.
- Success means verified proof URL, tweet id, or clear browser/profile proof.
- If proof is missing, report `attempted_without_proof`, not `published`.

## Learning Rule
- Learn after meaningful runs, but keep only distilled lessons active.
- Put quality examples in [[projects/ilindex/x-operator-golden-examples]].
- Put deep failures and diagnostics in [[projects/ilindex/x-operator-learning-school]].
- Put timing/tool-call evidence in [[projects/ilindex/x-operator-run-metrics]].

## Related
- [[projects/ilindex/x-operator]]
- [[projects/ilindex/x-operator-golden-examples]]
- [[projects/ilindex/x-operator-learning-school]]
- [[projects/ilindex/x-operator-run-metrics]]

