---
title: Hermes Credentials Directory
created: 2026-04-10
updated: 2026-04-10
type: summary
tags: [hermes, credentials, security, bridge]
sources: []
---

# Hermes Credentials Directory

## Purpose
This directory stores Hermes-side credential structure, machine context, and bridge context.

## Rules
- Durable docs here may be committed.
- Actual secrets must stay under `credentials/local/` only.
- Nothing under `credentials/local/` may be committed.
- Secrets copied from chat or screenshots are treated as exposed and must be rotated before live use.
- Jarvis canon and Jarvis vault are outside this directory.

## Files
- xai.env.example push-safe variable contract for x.ai / Grok access.
- `xai-management.env.example` push-safe variable contract for x.ai management access.
- `machine-and-bridge-context.md` non-secret machine, path, and bridge summary.
- `x-operator.env.example` push-safe variable contract for the X operator.
- `x-web.env.example` push-safe variable contract for the X browser login lane.
- `xai-account-canon.md` canonical identity and ownership note for x.ai, X, ILINDEX, and operator lanes.
- `local/` local-only secrets folder, git-ignored.

## Separation Rule
- `x.ai runtime` is inference-only and uses `XAI_API_KEY` from `local/xai.env`.
- `x.ai management` is admin-only and uses `XAI_MANAGEMENT_KEY` from `local/xai-management.env`.
- `X / Twitter operator` is a separate auth lane and uses `local/x-operator.env` plus `local/x-web.env`.
- Hermes-local runtime should mount or symlink these secrets through the active profile's `$HERMES_HOME/credentials/` when using `required_credential_files`.
- Do not reuse an x.ai management key for normal inference.
- Do not treat X Developer Platform billing as x.ai runtime truth.
