---
title: X Operator Run Metrics
created: 2026-05-02
updated: 2026-05-02
type: summary
tags: [ilindex, x-operator, diagnostics, runtime]
sources:
  - /home/rotemg/.hermes-twitter-operator/state.db
  - /home/rotemg/.hermes-twitter-operator/reports/approved-publish
  - /home/rotemg/.hermes-twitter-operator/reports/intervals
---

# X Operator Run Metrics

## Purpose
Use this page for diagnosis and optimization, not for normal prompt context.

## Key Metrics To Track
- `mode`: manual, cron, approved publish, training.
- `duration`: wall time from start to final response/proof.
- `api_call_count` and `tool_call_count`.
- `compression_count`: how many continuation segments were needed.
- `result`: shortlist, published, blocked, no-publish, stale.
- `proof`: direct X proof URL when published.

## Current Baseline
| Date | Mode | Result | Time / Calls | Evidence |
|---|---|---|---|---|
| 2026-05-02 13:00 | cron | published BEACON | about 6 minutes, 38 API calls | `https://x.com/ilindexbot/status/2050516616866103739` |
| 2026-05-01 21:00 | cron | published BEACON | about 6 minutes, 36 API calls | `https://x.com/ilindexbot/status/2050274935218524589` |
| 2026-05-01 17:00 | cron | published BEACON | about 8 minutes, 52 API calls | `https://x.com/ilindexbot/status/2050215364076683282` |
| 2026-05-01 00:29 | manual training | 6 useful candidates | report only, no publish | `training-shortlist-20260501_002952.md` |
| 2026-05-01 18:12 | manual optimized shortlist | 4 BEACON candidates | report only, no publish | `optimized-shortlist-20260501_1812.md` |
| 2026-05-02 13:12 | manual discovery | too long | about 90 API calls across continuation | stop future runs at budget and return partials |

## Diagnostic Rules
- Cron quality is currently acceptable; do not weaken cron because a manual deep-search run overran.
- Manual discovery should optimize for fast useful output, not exhaustive search.
- A session with `ended_at=null` after gateway restart may be stale. Validate by process/service state before treating it as active work.
- Compression during manual discovery is a signal to summarize and stop, not a license to continue deep research.

## Related
- [[projects/ilindex/x-operator]]
- [[projects/ilindex/x-operator-active-rules]]
- [[projects/ilindex/x-operator-learning-school]]

