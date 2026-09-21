---
name: design-deslop
description: Improve website and app designs. Remove unwanted patterns in text, typography, layout, color, and decoration. Use for interface changes, design reviews, and requests to deslop a design.
---

# Design Deslop

Make the interface suitable for its users, content, and task. Check the patterns listed below for specific problems. These patterns describe design preferences. They are not automatic reasons for removal and do not prove that AI made the interface.

Keep useful content, product functions, and accessibility features. Obey the user's design requirements. Keep required brand elements. An existing style is not automatically a requirement.

Words such as “modern,” “premium,” and “polished” do not permit unwanted patterns. Do not replace the design with another standard template. Do not remove useful color, shape, or content.

Fewer colors and less decoration are not goals by themselves. Keep visual choices that help users or give the product a distinct style. Give specialists the observed problem, intended result, and work limits. Let them choose a suitable correction within the user's requirements. Do not give broad instructions such as “reduce bright backgrounds” without identifying where those backgrounds cause a problem.

## Five review areas

Check the five areas in sequence. For a small interface, use one reviewer by default. Separate specialist subagents are optional when the work benefits from them. In either mode, read each area's reference, find useful improvements, make changes, and check the result.

When using specialists, the main agent acts as manager. It controls the work limits, transfers information, and checks the final result. When working alone, the main agent also does the review work. References to the manager then mean decisions or follow-up work for that same agent.

| Area | Reference | Patterns to inspect |
| --- | --- | --- |
| Copy: interface text | [copy.md](references/copy.md) | Unnecessary slogans, repeated help, decorative captions, repeated labels, and unnecessary technical claims |
| Typography: text styles | [typography.md](references/typography.md) | Unwanted default fonts, large uppercase labels above headings, and unclear text order |
| Layout: content arrangement | [layout.md](references/layout.md) | Too many cards, panels inside panels, and unnecessary rows of three numbers |
| Color | [color.md](references/color.md) | Purple without a clear purpose, bright gradients, and multicolor borders |
| Decoration | [decoration.md](references/decoration.md) | Large icon tiles, unnecessary left borders, excessive corner rounding, and large blurred shadows |

## Prepare the task

Identify the main user task, intended users, requirements, and files that can change. Read the applicable project rules. Identify existing user changes that must remain. Use package and source information already available when it is sufficient.

Inspect the source and the displayed interface. Check desktop and narrow screen sizes when possible. Do not determine the actual appearance from style values alone.

A request to improve an editable interface permits changes within the requested work. Do not add an approval step for recommendations. For a review-only request, use the same sequence without edits. If only an image is available, explain that changes require editable source. Do not claim that the interface changed.

Save useful screenshots before the first task. For full-page captures or before and after comparisons, read [screenshots.md](references/screenshots.md) before editing. Record the page, screen size, interface state, and whether each image shows the interface before or after changes. Use absolute paths to screenshots and source files.

Inspect saved images before using them as evidence. Follow the screenshot reference if capture fails. Report when visual checks are not possible. Keep requested before and after images and show them with clear labels in the final response.

## Run the sequence

Use this order: **Copy → Layout → Typography → Color → Decoration**.

Change content first, then structure, then appearance. Keep the five areas distinct and do not run change tasks at the same time. Obey a different order or smaller work limit specified by the user.

When working alone, use the inspect, change, and check steps below for each area. Keep a short work list and a record of visual checks. Carry decisions and incomplete work into the next area. Separate agent messages are not required.

### Optional specialist sequence

Send one area to one specialist at a time. Images and browser tabs in the manager's session might not be available to subagents. The manager makes browser captures and supplies new images when necessary. Do not make each specialist find the preview settings again.

For each task:

1. Send instructions that use the format below. Include earlier work lists and decisions. Identify screenshots that show the current interface.
2. Require the specialist to open the supplied images and confirm which paths it could inspect before making visual judgments. A supplied path alone does not confirm access. If access fails, supply accessible images or record the visual check as incomplete. Source checks can continue, but must not be reported as visual checks.
3. Let the specialist inspect and change the assigned files independently. Do not edit those files while the specialist works. Wait for its completion message. Do not request status repeatedly at short intervals.
4. Read its work list and record of visual checks. Make sure that the task is complete and unrelated files did not change. Return a specific defect to the specialist for correction before the next task. Do not request another general review.
5. Make new screenshots if changes affect the next specialist's visual checks. Send current source paths, images, and decisions to the next specialist. It must use the current result and confirm access to new images.

If no useful changes are necessary, return “No changes needed.” Do not force changes or repeat the full sequence.

If a specialist cannot continue, correct the cause, complete the work with the main agent, or identify the incomplete work. Start the next task only if that work can continue safely. If subagents are unavailable, use one reviewer. Report any resulting limit on the checks.

## Task instruction format

Give each specialist sufficient information to work independently:

- **Goal and mode:** interface, intended users, user task, and change or review-only mode.
- **Assignment:** one area, reference path, observed problems, intended result, permitted files, shared components, and excluded work. Do not prescribe a replacement style unless the user requires it.
- **Requirements:** brand rules, content, functions, accessibility features, project rules, and existing edits to keep.
- **Current state:** source paths, labeled screenshot paths, screen sizes, interface states, earlier work lists, and decisions to keep. Require confirmation that the images were opened.
- **Tools and checks:** known preview, build, and test commands; required checks; and how to request missing images.
- **Completion:** make useful improvements, check affected functions, and return the short work list below. In change mode, do not stop at recommendations.

Supply only applicable information and references. Do not request complete package lists, unrelated skill reads, or another full sequence of this skill.

## Inspect, change, check

Read the current source and inspect the supplied images before changes. Use the reference as design guidance. Do not treat it as a required number of defects. Keep useful design choices. Explain when no change is necessary.

Before each removal, identify the element, its current purpose, and the specific reason to remove it. A reason can be an observed problem or an explicit user requirement. “Cleaner,” “less busy,” and a match to a listed pattern are not sufficient reasons by themselves. Consider a smaller change that keeps the useful function or distinct style. If there is no specific reason, keep the element. This check does not require user approval.

Make related changes within the assigned area. Include small spacing or container changes necessary to keep the interface usable. Specialists must not create more subagents. Keep work lists in the task context; do not create external report files. Do not expand the task into a full redesign.

Keep unrelated user edits. Do not reverse an earlier task only because you prefer another design. If an earlier decision prevents a necessary correction, report the conflict and a specific solution to the manager.

Make routine decisions independently. Ask the manager only for missing information or decisions outside your task. The manager uses existing user instructions to resolve these questions. Ask the user only when an important choice or additional permission is necessary.

This skill does not permit new dependencies, publishing, deployment, or unrelated external actions.

Run checks suitable for the change and required by the project. Use existing function tests where applicable. Do not add tests that only repeat text or style values. Check affected desktop and narrow layouts and control states. Request new screenshots from the manager when necessary. Identify checks that were not completed.

Keep a short record of actual visual checks. For each checked page and state, record the screen size, image path or direct preview, whether it was checked before or after changes, and the result. Name states such as default, menu open, keyboard focus, empty, or error only when actually inspected. List affected states that were not checked and the reason. Do not infer checks of interactive states from a default-state image. Earlier images do not prove that later changes were checked.

For each area, keep a short work list in this format. Specialists return it to the manager:

**[Area] — Done** (or **No changes needed** / **Blocked**)

- Changes completed and their reasons. Include a specific reason for each removal. Group removals only when the same reason applies to all named elements.
- Files changed.
- Checks completed, results, and limits, including the record of pages, screen sizes, and states actually inspected.
- Decisions or incomplete work for the next task, if applicable.

For review-only requests, use **[Area] — Recommendations**. List proposed changes. Do not report proposed changes as completed work.

## Finish

After all tasks, inspect the complete result at desktop and narrow screen sizes. Check affected control states. Check the content arrangement, text wrapping, font loading, contrast, keyboard focus, data, and labels. Run applicable function checks.

Compare the result with the earlier interface. Ask both: “Is this clearer?” and “Did we remove something useful or distinctive?” Check the reasons for removals against the result. Restore or adjust elements when a change removed useful information, function, or distinct style without sufficient benefit or an explicit user requirement. If comparison evidence is missing, report that limit.

Use previous check results when they remain valid. Repeat checks only when later changes could affect their results.

Correct new defects directly, or return them to the responsible specialist with a specific correction task. Do not restart the full sequence.

When all work is complete, start the final response with a short list of the changes made. For review-only requests, list recommendations instead. If no changes were needed, state this. Then briefly report checked pages, screen sizes and states, and important unchecked states. Include requested before and after screenshots. Do not present five long reports or request approval for work already completed.
