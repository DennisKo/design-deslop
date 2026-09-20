---
name: design-deslop
description: Improve website and app designs by removing generic AI design patterns in copy, typography, layout, color, and decoration. Use when creating or refining interfaces, reviewing frontend designs or screenshots, or asked to deslop a design. Use sequential specialist subagents to find, implement, and verify improvements, with a short handoff after each pass.
---

# Design Deslop

Build an intentional interface suited to its content, audience, and task. Remove the unwanted defaults below and improve the composition they leave behind. Treat them as the user's design preferences, not a claim that a technique is universally bad or that an interface was made by AI.

Preserve product functionality, useful content, and accessibility. Honor explicit user requirements and mandated brand assets; an existing accidental default is not a mandate. Do not use broad requests such as “modern,” “premium,” or “polished” to justify the unwanted patterns. Do not replace them with a different stock template or make every interface monochrome, square, and empty.

## Five specialist passes

The manager runs one specialist subagent at a time. Each specialist reads its reference, finds useful improvements in the current design, implements them, checks the result, and returns a short done-list. The manager owns scope, handoffs, and final verification.

| Module | Reference | Patterns to remove or improve |
| --- | --- | --- |
| Copy | [copy.md](references/copy.md) | Useless slogans, repeated help, decorative captions, redundant eyebrow text, implementation bragging |
| Typography | [typography.md](references/typography.md) | Geist, Inter, Manrope, DM Sans, Satoshi, Instrument Serif; large uppercase words above headlines; weak type hierarchy |
| Layout | [layout.md](references/layout.md) | Everything as cards, nested colored/outlined boxes, generic rows of three counters |
| Color | [color.md](references/color.md) | Purple everywhere, purple gradients, neon gradient elements and borders |
| Decoration | [decoration.md](references/decoration.md) | Huge rounded Lucide icon tiles above headings, left-border text boxes, excessive rounding, huge soft shadows |

## Manager: prepare the task

Establish the interface's main task, audience, explicit constraints, and files in scope. Inspect relevant source and rendered desktop and narrow views when available. Read applicable project rules and identify existing changes that must be preserved. Reuse sufficient package and source information already available.

A request to improve or deslop an editable interface authorizes implementation within that scope. Do not add a recommendation approval step. If the user asks only for a review, run the same sequence without edits and return recommendations. If only an image is available, explain that implementation needs editable source; do not claim to have changed the interface.

Save useful screenshots before the first pass. Give subagents absolute image and source paths; conversation images, browser bindings, and tab IDs may not be shared. The manager owns browser capture and can supply fresh evidence when requested. Do not make each specialist rediscover the preview setup.

Inspect captures for missing sections, clipping, repetition, and stitching errors. Prefer a supported direct full-page capture when needed. If capture fails, change the method or use labeled viewport images; do not repeatedly use a broken method. State when rendered evidence is unavailable.

If before/after screenshots are requested, save the before image before any edits. Use the same viewport width, scale, and UI state for the after image; page height can change. Keep both files and show them in the final response.

## Manager: run the sequence

Default order: **Copy → Layout → Typography → Color → Decoration**. Content changes come first, then structure, then visual treatment. Use a separate specialist for each pass. Do not combine the areas or run implementation passes in parallel. Follow a different order or narrower scope if the user specifies one.

For each pass:

1. Send the specialist an actionable brief using the contract below. Include the previous specialists' done-lists and decisions, and identify which screenshots show the current state.
2. Let the specialist inspect and implement autonomously within its assignment. The manager must not edit the same files while the specialist is working. Wait for completion notifications or use bounded waits; avoid frequent status polls.
3. Read the done-list and inspect the actual changes. Confirm that the assigned work is complete and no unrelated changes were made. Return a specific defect to that specialist for correction before moving on; do not request another broad review.
4. Refresh affected visual evidence when changes alter what the next specialist will assess. Pass the updated source, evidence, and decisions to the next specialist. A later specialist must work from the current result, not the original screenshot.

A pass with no useful changes returns “No changes needed.” Do not force edits or run repeated full cycles. If a specialist is blocked, address the specific cause or record the unfinished work. Continue to the next pass only when it can safely proceed with the actual state. If subagents are unavailable, disclose this and perform the same passes sequentially in the main agent.

## Specialist brief contract

The manager supplies enough context for independent work:

- **Goal and mode:** the interface, audience, user task, and implementation or review-only mode.
- **Assignment:** one area, its reference path, allowed files and shared components, and clear exclusions.
- **Constraints:** brand requirements, meaningful content, functionality and accessibility to preserve, project rules, and pre-existing edits.
- **Current state:** source paths, accessible screenshot paths with viewport/state details, previous done-lists, and decisions that must remain in effect.
- **Execution and checks:** relevant preview/build/test commands already discovered, required checks, and how to request missing visual evidence from the manager.
- **Completion:** implement justified improvements, verify affected behavior, and return the short done-list below. Do not stop at a proposal in implementation mode.

Give only relevant context and references. Do not require broad package inventories, unrelated skill reads, or another full round of this skill.

## Specialist: find, implement, check

Inspect current source and supplied visual evidence before choosing changes. Do not infer actual appearance from style tokens alone. Use the area's reference as design guidance, not a quota of defects. Preserve intentional treatments and explain when no change is needed.

Make cohesive changes within the assigned area, including small dependent spacing or wrapper fixes needed to leave the interface usable. Do not delegate further, create external report files, or expand into a full redesign. Preserve unrelated user edits. Do not undo an earlier pass merely to express a different preference. If an earlier decision prevents a necessary fix, report the conflict and a concrete resolution to the manager.

Resolve routine implementation details autonomously. Ask the manager only for missing information or decisions outside the assignment. The manager uses existing user instructions to resolve them and asks the user only when a material choice or additional authorization is actually needed. This skill does not authorize new dependencies, publishing, deployment, or unrelated external actions.

Run checks proportional to the change and required by the project. Use existing behavior tests where relevant; do not add tests that merely repeat copy or styling. Inspect affected desktop and narrow layouts and interactive states using available evidence. Request an updated capture from the manager when needed. State unverified behavior honestly.

Return this compact handoff in the conversation:

**[Area] — Done** (or **No changes needed** / **Blocked**)
- Concrete changes completed and why, usually 2–5 bullets.
- Files changed.
- Checks run and their results; state any limits.
- Decisions or unfinished work the next pass needs, only when relevant.

For review-only requests, use **[Area] — Recommendations**, with proposed changes instead of a done-list. Never label unimplemented recommendations as completed work.

## Manager: finish

After all passes, inspect the combined result at representative desktop and narrow sizes and affected interactive states. Check composition, text wrapping and font loading, contrast and focus visibility, preserved data and labels, and relevant existing behavior checks. Reuse checks that remain valid; repeat them only when later changes could affect their result.

Resolve regressions with targeted follow-ups to the responsible specialist. Do not restart the entire sequence. Report completed changes, checks, and material limits in one concise final response. Include requested before/after screenshots. Do not present five long audit reports or ask for retroactive approval of completed work.
