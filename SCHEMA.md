# Hermes Wiki Schema

## Domain
Hermes operational knowledge. This wiki stores bounded working knowledge for Hermes across bridge packets, ILINDEX analysis, OpenClaw support, and repeatable operational playbooks.

## Authority Model
- Jarvis is the canonical source of truth.
- Hermes is the operational memory and synthesis layer.
- The bridge is the only approved handoff path between Hermes and Jarvis.
- Hermes must never write to the Jarvis vault.
- Jarvis must never depend on this wiki as canon.

## Conventions
- File names: lowercase, hyphens, no spaces.
- Every durable page uses YAML frontmatter.
- Use [[wikilinks]] for internal references.
- Every meaningful update bumps the updated date.
- Every new durable page is added to index.md.
- Every ingest, decision, or structural change is logged in log.md.

## Frontmatter

```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | project | playbook | decision | summary
tags: [tag-one, tag-two]
sources: []
---
```

## Tag Taxonomy
- bridge
- packet
- hermes
- jarvis
- ilindex
- openclaw
- seo
- metadata
- routing
- marketing
- protocol
- authority
- decision
- playbook
- diagnostics
- content-strategy
- security
- x-operator

Rule: add new tags here before using them.

## Page Thresholds
- Create a page when the topic is reused, repeated, or central to a workstream.
- Add to an existing page when the new material extends an existing topic.
- Do not create pages for passing mentions or transient noise.
- Split a page when it becomes too large to scan quickly.

## Raw Sources
- raw/ is immutable source storage.
- Raw files are never edited in place.
- Summaries and synthesis belong outside raw/.

## Update Policy
- Newer, validated information supersedes older working notes.
- Conflicts should be recorded explicitly and linked.
- Unvalidated claims must be marked as inferred or blocked.

## Cross-Link Rule
Every durable page should link to at least two relevant pages when possible.
## Secure And Credential Material
- `credentials/` stores push-safe credential contracts and machine context.
- `credentials/local/` stores local-only secrets and is always git-ignored.
- Do not copy raw secrets into durable pages, bridge packets, or committed notes.
- Secrets seen in chat or screenshots must be rotated before live production use.

