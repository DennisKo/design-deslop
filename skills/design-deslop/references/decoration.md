# Decorative elements

Improve elements that remain after the earlier tasks. Keep the Layout task's decisions about containers. Make changes and check the result unless the user requested review only.

## Inspect

Find these patterns:

- Large icons in rounded, colored tiles above each heading. The Lucide icon library is not itself a defect.
- Colored left borders that give ordinary text unnecessary emphasis.
- Large rounded corners on all panels, images, fields, menus, and buttons, regardless of their size or function.
- Large blurred shadows around static content without a useful purpose.

## Improve

1. Remove icon backgrounds and large heading icons when they add no information. Keep useful icons. Match their size and alignment to nearby text. Keep accessible names for controls that contain only an icon.
2. Use ordinary text without decorative side borders. Use spacing, headings, or existing text styles to identify groups. Keep distinct styles for alerts, quotations, and states when useful. Do not use color as the only signal.
3. Use a small, consistent set of corner sizes. Match corners to component size and the product design. Keep pill shapes for suitable controls and labels. Do not remove all rounded corners automatically.
4. Remove unnecessary shadows from static sections. Keep limited shadows for overlays, floating controls, and movable items when they help users understand position or operation. Use dividers, background contrast, or spacing when sufficient.

## Check and report

Check desktop and narrow layouts. Inspect available hover, focus, disabled, and open states.

Make sure that controls remain easy to identify and keyboard focus remains visible. Overlays must remain distinct from underlying content. Check that shadows do not cause cut edges or unnecessary scrolling. Remove empty containers and correct gaps after icon removal.

Use the short work-list format in SKILL.md. Identify decorative changes, affected shared styles, and check limits. Keep unrelated components unchanged.

For review-only requests, return recommendations. Do not create report files or more subagents.
