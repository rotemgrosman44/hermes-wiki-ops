---
title: ADHD-First Hermes Web UI
created: 2026-04-17
updated: 2026-04-17
type: project
tags: [hermes, ui, adhd, human-loop, authority]
sources: []
---

# ADHD-First Hermes Web UI

## Goal
Make the Hermes dashboard easier for Rotem to scan, remember, and trust without opening alternate task-specific screens.

## Canonical Entry
- `Canonical Surfaces` is the single visual entry point.
- New task work should extend the existing tab structure, not create competing dashboard surfaces.
- `Canonical Surfaces` is the first screen for orientation, not a temporary task-specific skin.

## Problems To Solve
- Too much text before the user understands who is who.
- Drift between live runtime truth and what the screen appears to say.
- Approval points are too easy to miss.
- Raw operational detail can bury the human decision point.
- Long continuous dark-green surfaces can cause orientation loss during scrolling.

## Rotem Focus Skin
- Personal profile name: `Rotem Focus`
- Default mode: dark only
- Mood: Hermes + Matrix + ILINDEX
- Visual rule: keep the green atmosphere, but split the screen into clearly different zones instead of one continuous slab
- Scope: this is a productivity skin for Hermes Web UI on the laptop, not a runtime redesign
- Language rule:
  - English headline first
  - Hebrew functional helper second
  - Hebrew helper should explain action, not marketing mood

## Canonical Identity Labels
- Backend identity stays unchanged:
  - Hermes main runtime id: `madhatter`
- Visible main label in the UI:
  - `Hermes - The Mad Hatter / WhatsApp`
- Twitter operator visible label:
  - `Hermes Twitter Operator / Telegram`
- Jarvis stays visually separate:
  - `Jarvis MAIN / External Portal`
- Visual labels may be friendlier than backend ids, but runtime truth must remain untouched.

## First Visual Rules
- Keep a fixed visual distinction between `Main`, `Operator`, and `External`.
- Use short labels and a small number of stable status words.
- Surface only three high-level questions first:
  - what is live now
  - where Rotem is needed
  - what is external / hands-off
- Push diagnostic files and authority paths behind a lower-noise detail layer.

## Band Structure
The page should read as three clear visual bands:

1. Orientation band
   - `Canonical Surfaces`
   - current runtime
   - one-sentence explanation of how to use the page

2. Summary band
   - `Running Now`
   - `Needs Rotem`
   - `Hands Off`

3. Control surfaces band
   - individual cards for `Main`, `Operator`, `External`
   - deeper paths and commands hidden under `More details`

4. Right action panel
   - fixed on desktop
   - stacked above or below on smaller widths
   - contains the canonical operational commands and recovery paths

These bands must remain visually distinct during scroll by background change, border treatment, and heading scale.

## Human Entry Model
- `Needs Rotem` means approval, pairing, or explicit human confirmation.
- `Running` means live and operational.
- `Blocked` means lane failure or missing prerequisite.
- `External` means visible but not part of Hermes runtime state.
- Only these four human-readable states are allowed on first glance.
- `Needs Rotem` should be explained as one of two human gates:
  - `Technical intervention`
  - `Men in the loop`
- `External` must look neutral, not broken.

## Traffic-Light Model
- `Running` = green
- `Needs Rotem` = amber
- `Blocked` = red
- `External` = neutral slate / blue-grey
- The state color must work like a quick traffic-light scan before reading text.

## Contrast Rules
- Major headings should be near-white, not muted cream.
- Section titles should be brighter than surrounding body copy.
- Body text can stay warm/off-white, but action labels must be stronger.
- Borders should be visible enough to form memory anchors.
- Important action areas should use a warmer highlighted frame, not only text color.

## Logo and Icon Rules
- Use larger branded marks for first-glance recognition:
  - WhatsApp for Hermes main
  - Telegram for Twitter operator
  - Jarvis-specific external mark for Jarvis portal
- Logo position must stay stable inside each card.
- Brand marks help orientation; they are not decorative chrome.
- If a production-safe local Mad Hatter avatar asset is later added, it can be used as the main visual identity anchor, but the UI must not depend on that asset existing.

## Pending Character Notes
- When we reach the relevant character/avatar tab in the Web UI, check the built-in gallery first before introducing any custom character system.
- Prefer a built-in option if it fits the current kawaii / friendly agent direction and does not break the existing architecture.
- Keep this as a later visual pass; do not steer the current dashboard work toward character redesign yet.
- Add one future research item:
  - identify the famous game/world reference Rotem mentioned and evaluate whether it fits the Hermes character lane without causing visual drift.
- Apply this only in the correct UI area for agent character/identity customization, not in unrelated tabs.

## Heading Hierarchy
- Loudest text on the screen:
  - `Canonical Surfaces`
- Hebrew helper directly under it:
  - `כאן מתחילים`
- Loudest text inside a card:
  - visible surface label
- Next:
  - role badge + state badge
- Then:
  - short action or boundary explanation
- Lowest layer:
  - runtime paths, authority files, canonical commands

## Human-Gate Placement
- Every card exposes at most one first-glance action zone.
- Human-gated areas must sit above diagnostic depth.
- Approval/pairing/re-pair notes go into the action section, not buried in details.
- `Hands Off` information should be visible without opening card details.
- Operational commands that help Rotem recover or inspect the system belong in the right-side action panel, not scattered across the page.

## Right Action Panel
- The panel is the canonical place for:
  - main checks
  - operator checks
  - logs
  - recursive loop locations
  - Mac coordination pack paths
- The panel should answer: `איך מטפלים עכשיו`
- It must stay stable from session to session so Rotem builds muscle memory.

## Mac Coordination Rule
- Do not change Hermes/Jarvis wiki architecture from the laptop alone.
- Coordination artifacts for Codex/Jarvis on the Mac must be prepared first on the Hermes side as bounded runbooks/prompts.
- No direct write into `jarvis-canon` from the laptop lane.

## No Competing Surfaces Rule
- Do not create alternate dashboard home screens for temporary tasks.
- Do not solve drift by spawning a separate visual surface.
- Add tabs only when they extend the canonical structure.
- `Canonical Surfaces` stays the fixed orientation anchor across updates.

## Phase Order
1. `Surfaces`
2. `Status`
3. `Cron`
4. `Approvals`

## Related
- [[concepts/protocols/canonical-identity-map]]
- [[entities/people/rotem-grossman]]
- [[projects/hermes/hermes]]
