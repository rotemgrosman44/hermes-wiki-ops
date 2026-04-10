---
title: Checksum Validation
created: 2026-04-10
updated: 2026-04-10
type: playbook
tags: [playbook, packet, diagnostics]
sources: []
---

# Checksum Validation

## Standard Flow
1. Read the packet manifest first.
2. Confirm every required file exists.
3. Validate provided hashes before any synthesis work.
4. Stop the run if a required file is missing or a checksum mismatches.
5. Record the result in log.md when the validation is meaningful to future work.

## Rule
Checksum validation happens before interpretation, not after.

## Related
- [[playbooks/packet-intake]]
- [[playbooks/return-packaging]]
