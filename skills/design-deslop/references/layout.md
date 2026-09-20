# Layout and grouping

Inspect and improve the current layout within the manager’s assignment. Implement useful structural changes and verify the result unless the user requested review only. Preserve content decisions from the Copy pass.

## Detect

- **Cardocalypse:** every heading, paragraph, statistic, or control occupies a separate card. Nested cards repeat backgrounds, outlines, padding, and corner treatments without expressing meaningful containment.
- **Boxes in boxes:** colored panels inside outlined panels inside another section wrapper make the page harder to scan than the content requires. Identify which boundaries represent real groups and which merely decorate them.
- **The three-counter strip:** three equally prominent adjacent numbers appear because the template expects a proof section. Look for redundant metrics, invented claims, missing context, and numbers disconnected from the user's decision.

Inspect the actual content hierarchy, interaction boundaries, reading order, responsive behavior, and existing design system before choosing a replacement.

## Improve

Remove ornamental wrappers by default. Group related content with spacing, alignment, a shared heading, or a restrained divider. Use a plain list for related items, a table for comparisons, and a continuous section for one narrative. Preserve a card when it represents an independently actionable entity, such as a product or project, or when its boundary makes a genuine grouping clearer. Do not impose one replacement layout across every section.

Replace the reflexive three-counter strip with the presentation the evidence deserves. A single important measure can accompany its explanation; comparative measures may belong in a table or chart; supporting facts can sit beside the claim they substantiate. Preserve useful data, units, timeframes, and source context. Flag unsupported claims rather than inventing evidence or silently rewriting values. Three metrics may remain when their grouping supports a concrete decision.

## Verify and report

Check that removing wrappers preserves reading order, control relationships, clickable targets, focus visibility, and responsive flow. Confirm that meaningful groups remain identifiable without decorative nesting and useful metrics remain available.

Report structural changes and affected shared components. Pass any remaining typography, color, or decoration dependencies to the manager. State when an apparent pattern is justified and should remain.

Return the short specialist handoff defined in SKILL.md: completed changes, files, checks, and any limits or dependencies. In review-only mode, report recommendations instead. Do not create report files or start another round of subagents.
