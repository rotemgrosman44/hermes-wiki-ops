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
- `machine-and-bridge-context.md` non-secret machine, path, and bridge summary.
- `x-operator.env.example` push-safe variable contract for the X operator.
- `local/` local-only secrets folder, git-ignored.
