---
title: X Operator Learning School
created: 2026-05-02
updated: 2026-05-02
type: playbook
tags: [ilindex, x-operator, diagnostics, playbook, runtime]
sources:
  - /home/rotemg/.hermes-twitter-operator/reports
  - /mnt/c/Users/user/.codex/skills/recursive-learning-hermes-growth/SKILL.md
---

# X Operator Learning School

## Purpose
This is the deeper learning layer for deliberate improvement and diagnosis. It is not loaded by default in normal runs.

## Learning Technique
Use atomic recursive learning:
1. Observe a run.
2. Separate evidence from interpretation.
3. Distill one operational lesson.
4. Promote to Active Rules only if it is repeated, high-impact, or safety-critical.
5. Store examples separately from rules.
6. Store metrics separately from examples.

## Context Budgeting
- Default context: runbook plus [[projects/ilindex/x-operator-active-rules]].
- Quality context: add [[projects/ilindex/x-operator-golden-examples]].
- Diagnosis context: add this page and [[projects/ilindex/x-operator-run-metrics]].
- Raw reports are read by targeted lookup only.

## Lessons

### Long Manual Discovery Chain
- Symptom: a manual shortlist run searched correctly but crossed multiple continuation/compression segments and reached about 90 API calls.
- Root cause: the operator treated manual discovery like deep research.
- Correction: manual discovery must return partial candidates or `blocked_by_iteration_budget` when the fast budget is hit.
- Guard: compression during manual shortlist mode means summarize and stop.

### Disabled Skill Noise
- Symptom: cron output exposed warnings that old X skills were listed but disabled.
- Root cause: runbook/job skill list drifted from runtime `config.yaml`.
- Correction: keep the active stack lean and aligned with actually available skills.
- Guard: if a skill is disabled in config, it must not be presented as active operator truth.

### Learning/Wiki Noise In User Reports
- Symptom: reports mentioned Wiki paths, section names, or raw learning-line language.
- Root cause: internal durable memory leaked into user-facing Telegram output.
- Correction: user reports may say only `נשמר כלל תפעולי פנימי: <lesson>`.
- Guard: storage mechanics are internal unless Rotem explicitly asks where something was saved.

### Proof Before Success
- Symptom: browser sends can show toast, composer reset, or lagging DOM.
- Root cause: X UI state is not enough proof.
- Correction: verify through direct proof URL, profile replies, exact phrase search, or browser-visible reply card.
- Guard: no proof means `attempted_without_proof`.

### Source Quality Over Volume
- Symptom: broad seeds like `סוכנים` can drift into political/noisy or generic posts.
- Root cause: the keyword is too broad for high-fit Hebrew operator work.
- Correction: prefer narrower terms around Claude Code, Codex, local models, permissions, memory, tests, workflow, agents, and cost friction.
- Guard: fewer strong candidates beat a padded list.

## Promotion Rules
- Promote to [[projects/ilindex/x-operator-active-rules]] when a lesson protects publish safety, runtime authority, or bounded run time.
- Keep in [[projects/ilindex/x-operator-golden-examples]] when a lesson is mainly about style or quality.
- Keep here when a lesson is diagnostic, rare, or too detailed for normal runs.

## Related
- [[projects/ilindex/x-operator]]
- [[projects/ilindex/x-operator-active-rules]]
- [[projects/ilindex/x-operator-golden-examples]]
- [[projects/ilindex/x-operator-run-metrics]]

