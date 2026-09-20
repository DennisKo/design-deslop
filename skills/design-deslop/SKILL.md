---
name: design-deslop
description: Improve website and app designs. Remove unwanted patterns in text, typography, layout, color, and decoration. Use for interface changes, design reviews, and requests to deslop a design. Send one specialist subagent at a time to find, make, and check improvements.
---

# Design Deslop

Make the interface suitable for its users, content, and task. Remove the unwanted patterns listed below. These patterns describe design preferences. They do not prove that AI made the interface.

Keep useful content, product functions, and accessibility features. Obey the user's design requirements. Keep required brand elements. An existing style is not automatically a requirement.

Words such as “modern,” “premium,” and “polished” do not permit unwanted patterns. Do not replace the design with another standard template. Do not remove useful color, shape, or content.

## Five specialist tasks

The manager sends one task to one specialist subagent at a time. Each specialist reads its reference, finds improvements, makes changes, and checks the result. It then returns a short list of completed work. The manager controls the work limits, transfers information, and checks the final result.

| Area | Reference | Patterns to remove or improve |
| --- | --- | --- |
| Copy: interface text | [copy.md](references/copy.md) | Unnecessary slogans, repeated help, decorative captions, repeated labels, and unnecessary technical claims |
| Typography: text styles | [typography.md](references/typography.md) | Unwanted default fonts, large uppercase labels above headings, and unclear text order |
| Layout: content arrangement | [layout.md](references/layout.md) | Too many cards, panels inside panels, and unnecessary rows of three numbers |
| Color | [color.md](references/color.md) | Purple without a clear purpose, bright gradients, and multicolor borders |
| Decoration | [decoration.md](references/decoration.md) | Large icon tiles, unnecessary left borders, excessive corner rounding, and large blurred shadows |

## Manager: prepare the task

Identify the main user task, intended users, requirements, and files that can change. Read the applicable project rules. Identify existing user changes that must remain. Use package and source information already available when it is sufficient.

Inspect the source and the displayed interface. Check desktop and narrow screen sizes when possible. Do not determine the actual appearance from style values alone.

A request to improve an editable interface permits changes within the requested work. Do not add an approval step for recommendations. For a review-only request, use the same sequence without edits. If only an image is available, explain that changes require editable source. Do not claim that the interface changed.

Save useful screenshots before the first task. Supply absolute paths to screenshots and source files. Images and browser tabs in the manager's session might not be available to subagents. The manager makes browser captures and supplies new images when necessary. Do not make each specialist find the preview settings again.

Check screenshots for missing content, cut edges, repeated sections, and incorrect image joins. Use a supported full-page capture method when necessary. If it fails, change the method or use labeled images of the visible page area. Do not repeat a failed capture method. Report when visual checks are not possible.

If the user requests before and after screenshots, save the before image before changes. Use the same page width, scale, and interface state for the after image. The page height can change. Keep both files and show them in the final response.

## Manager: run the sequence

Use this order: **Copy → Layout → Typography → Color → Decoration**.

Change content first, then structure, then appearance. Use a separate specialist for each area. Do not combine areas or run change tasks at the same time. Obey a different order or smaller work limit specified by the user.

For each task:

1. Send instructions that use the format below. Include earlier work lists and decisions. Identify screenshots that show the current interface.
2. Let the specialist inspect and change the assigned files independently. Do not edit those files while the specialist works. Wait for its completion message. Do not request status repeatedly at short intervals.
3. Read its work list and inspect the changes. Make sure that the task is complete and unrelated files did not change. Return a specific defect to the specialist for correction before the next task. Do not request another general review.
4. Make new screenshots if changes affect the next specialist's visual checks. Send current source paths, images, and decisions to the next specialist. It must use the current result.

If no useful changes are necessary, return “No changes needed.” Do not force changes or repeat the full sequence.

If a specialist cannot continue, correct the cause or identify the incomplete work. Start the next task only if that work can continue safely. If subagents are unavailable, tell the user. Complete the same tasks in sequence with the main agent.

## Task instruction format

Give each specialist sufficient information to work independently:

- **Goal and mode:** interface, intended users, user task, and change or review-only mode.
- **Assignment:** one area, reference path, permitted files, shared components, and excluded work.
- **Requirements:** brand rules, content, functions, accessibility features, project rules, and existing edits to keep.
- **Current state:** source paths, available screenshot paths, screen sizes, interface states, earlier work lists, and decisions to keep.
- **Tools and checks:** known preview, build, and test commands; required checks; and how to request missing images.
- **Completion:** make useful improvements, check affected functions, and return the short work list below. In change mode, do not stop at recommendations.

Supply only applicable information and references. Do not request complete package lists, unrelated skill reads, or another full sequence of this skill.

## Specialist: inspect, change, check

Read the current source and inspect the supplied images before changes. Use the reference as design guidance. Do not treat it as a required number of defects. Keep useful design choices. Explain when no change is necessary.

Make related changes within the assigned area. Include small spacing or container changes necessary to keep the interface usable. Do not create more subagents or external report files. Do not expand the task into a full redesign.

Keep unrelated user edits. Do not reverse an earlier task only because you prefer another design. If an earlier decision prevents a necessary correction, report the conflict and a specific solution to the manager.

Make routine decisions independently. Ask the manager only for missing information or decisions outside your task. The manager uses existing user instructions to resolve these questions. Ask the user only when an important choice or additional permission is necessary.

This skill does not permit new dependencies, publishing, deployment, or unrelated external actions.

Run checks suitable for the change and required by the project. Use existing function tests where applicable. Do not add tests that only repeat text or style values. Check affected desktop and narrow layouts and control states. Request new screenshots from the manager when necessary. Identify checks that were not completed.

Return a short response in this format:

**[Area] — Done** (or **No changes needed** / **Blocked**)

- Changes completed and their reasons, usually 2–5 items.
- Files changed.
- Checks completed, results, and limits.
- Decisions or incomplete work for the next task, if applicable.

For review-only requests, use **[Area] — Recommendations**. List proposed changes. Do not report proposed changes as completed work.

## Manager: finish

After all tasks, inspect the complete result at desktop and narrow screen sizes. Check affected control states. Check the content arrangement, text wrapping, font loading, contrast, keyboard focus, data, and labels. Run applicable function checks.

Use previous check results when they remain valid. Repeat checks only when later changes could affect their results.

Return new defects to the responsible specialist with a specific correction task. Do not restart the full sequence. Report completed changes, checks, and important limits in one short final response. Include requested before and after screenshots. Do not present five long reports or request approval for work already completed.
