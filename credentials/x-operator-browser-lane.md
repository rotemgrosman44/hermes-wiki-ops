---
title: X Operator Dedicated Browser Lane
created: 2026-04-10
updated: 2026-04-10
type: credential-note
tags: [x-operator, browser, remote-debugging, hermes]
sources: []
---

# X Operator Dedicated Browser Lane

## Decision
Hermes uses a dedicated Chrome profile for X web operations.

## Why
- Stable remote control over an existing browser session.
- No dependence on Rotem's daily Chrome tabs.
- Session can be reused across runs.
- Better fit for remote operation and later unattended execution.

## Canonical Windows Paths
- Chrome launcher script:
  - `D:\hermes2-boys2\workspace\hermes-home\tools\x-web-operator\start-operator-browser.ps1`
- Shared browser helpers:
  - `D:\hermes2-boys2\workspace\hermes-home\tools\x-web-operator\shared.js`
- Publish lane:
  - `D:\hermes2-boys2\workspace\hermes-home\tools\x-web-operator\publish-replies.js`
- Dedicated Chrome user data dir:
  - `D:\hermes2-boys2\workspace\hermes-home\state\x-operator-chrome`
- Remote debugging endpoint:
  - `http://127.0.0.1:9223`

## Operational Rule
- Hermes attaches to the dedicated Chrome profile.
- Hermes does not depend on the human Chrome profile.
- If the profile is already authenticated, Hermes skips login bootstrap.
- Login bootstrap is fallback only.

## Current Validation
- Attach over CDP: validated.
- X home load in dedicated profile: validated.
- Live publish via dedicated profile: validated.

## Caveat
- X web still has intermittent UI guards and duplicate checks.
- For already-posted replies, X returns duplicate-style guard text.
- For reliable unattended operation later, the dedicated profile should stay warm and logged in.
